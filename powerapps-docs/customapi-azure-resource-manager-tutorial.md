---
title: "Azure Active Directory とカスタム コネクタを使用する | Microsoft Docs"
description: "Azure Resource Manager 用のカスタムコネクタを作成し、Azure Active Directory の認証を使用する方法を説明します。"
services: 
suite: powerapps
documentationcenter: 
author: mgblythe
manager: anneta
editor: 
ms.service: powerapps
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/03/2017
ms.author: mblythe
ms.openlocfilehash: b3df99a335947b0472b9230090e6a49fcea0f799
ms.sourcegitcommit: 68eee592c351688e5d0bd458f33a70be507fa53f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2018
---
# <a name="use-azure-active-directory-with-a-custom-connector-in-powerapps"></a>PowerApps で Azure Active Directory とカスタム コネクタを使用する
Azure Resource Manager (ARM) を使用して、データベース、仮想マシン、Web アプリなどのソリューションのコンポーネントを Azure で管理できます。 このチュートリアルでは、Azure Active Directory で認証を有効にし、ARM API の 1 つをカスタム コネクタとして登録した後、PowerApps でそのコネクタに接続する方法を示します。 これは、Azure のリソースをアプリから直接管理する場合に便利な方法です。 ARM の詳細については、「[Azure Resource Manager の概要](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-overview)」を参照してください。

## <a name="prerequisites"></a>前提条件
* [Azure サブスクリプション](https://azure.microsoft.com/free/)。
* [PowerApps アカウント](https://powerapps.microsoft.com)。
* このチュートリアルで使用する[サンプルの OpenAPI ファイル](http://pwrappssamples.blob.core.windows.net/samples/AzureResourceManager.json)。

## <a name="enable-authentication-in-azure-active-directory"></a>Azure Active Directory で認証を有効にする
最初に、ARM API エンドポイントの呼び出し時に認証を実行する Azure Active Directory (AAD) アプリケーションを作成する必要があります。

1. [Azure Portal](https://portal.azure.com) にサインインします。  Azure Active Directory テナントが複数ある場合は、右上隅のユーザー名を確認して、適切なディレクトリにログインしていることを確認します。
   
    ![ユーザー名](./media/customapi-azure-resource-manager-tutorial/current-user.png)
2. 左側のメニューの **[その他のサービス]** をクリックします。  **[フィルター]** ボックスに「**Azure Active Directory**」と入力し、**[Azure Active Directory]** をクリックします。
   
    ![Azure Active Directory](./media/customapi-azure-resource-manager-tutorial/azureaad.png)
   
    [Azure Active Directory] ブレードが開きます。   
3. [Azure Active Directory] ブレードのメニューで、**[アプリの登録]** をクリックします。
   
    ![アプリの登録](./media/customapi-azure-resource-manager-tutorial/azureapplication.png)
4. 登録済みのアプリケーションの一覧で **[追加]** をクリックします。
   
    ![[追加] ボタン](./media/customapi-azure-resource-manager-tutorial/add-app-btn.png)   
5. アプリケーション名を入力し、**[Web アプリ/API]** を選択したままにして、**[サインオン URL]** に「`https://login.windows.net`」と入力します。  **[作成]** をクリックします。  
   
    ![新しいアプリのフォーム](./media/customapi-azure-resource-manager-tutorial/newapplication.png)
6. 一覧にある新しいアプリケーションをクリックします。
   
    ![一覧の新しいアプリ](./media/customapi-azure-resource-manager-tutorial/newapplication2.png)
   
    [登録済みのアプリ] ブレードが開きます。  **アプリケーション ID** を書き留めておきます。  これは後で必要になります。
7. [設定] ブレードも開いています。  開いていない場合は、**[設定]** をクリックします。
   
    ![[設定] ボタン](./media/customapi-azure-resource-manager-tutorial/settings-btn.png)
8. [設定] ブレードで、**[応答 URL]** をクリックします。 URL の一覧で、`https://msmanaged-na.consent.azure-apim.net/redirect` を追加し、**[保存]** をクリックします。
   
    ![[応答 URL]](./media/customapi-azure-resource-manager-tutorial/reply-urls.png)
9. [設定] ブレードに戻り、**[必要なアクセス許可]** をクリックします。  [必要なアクセス許可] ブレードで、**[追加]** をクリックします。
   
    ![[必要なアクセス許可]](./media/customapi-azure-resource-manager-tutorial/permissions.png)
   
    [API アクセスの追加] ブレードが開きます。
10. **[API を選択します]** をクリックします。 表示されたブレードで、Azure Service Management API のオプションをクリックし、**[選択]** をクリックします。
    
    ![API の選択](./media/customapi-azure-resource-manager-tutorial/permissions2.png)
11. **[アクセス許可を選択します]** をクリックします。  *[委任されたアクセス許可]* で **[Access Azure Service Management as organization users (組織ユーザーとして Azure Service Management にアクセスする)]** をクリックし、**[選択]** をクリックします。
    
    ![[委任されたアクセス許可]](./media/customapi-azure-resource-manager-tutorial/permissions3.png)
12. [API アクセスの追加] ブレードで、**[完了]** をクリックします。
13. [設定] ブレードに戻り、**[キー]** をクリックします。  [キー] ブレードで、キーの説明を入力し、有効期限を選択して、**[保存]** をクリックします。  新しいキーが表示されます。  このキーの値を書き留めておきます。これも後で必要になります。  これで Azure Portal を閉じることができます。
    
    ![キーの作成](./media/customapi-azure-resource-manager-tutorial/configurekeys.png)

## <a name="add-the-connection-in-powerapps"></a>PowerApps で接続を追加する
AAD アプリケーションが構成されたので、カスタム コネクターを追加します。

1. [powerapps.com](https://web.powerapps.com) の左側のメニューで、**[接続]** を選択します。 省略記号 (**...**) を選択し、右上隅の **[Manage custom connectors]** (カスタム コネクタの管理) を選択します。
   
     > [!TIP]
> モバイル ブラウザーでカスタム コネクタを管理する場所が見つからない場合は、左上隅のメニューの下にある可能性があります。
   
    ![カスタム コネクタの作成](./media/customapi-azure-resource-manager-tutorial/managecustomapi.png)  
2. **[Create custom connector]** (カスタム コネクタの作成) を選択します。
   
    ![カスタム コネクタのプロパティ](./media/customapi-azure-resource-manager-tutorial/newcustomapi.png)
3. 接続の名前を入力し、[サンプルの ARM OpenAPI ファイル](http://pwrappssamples.blob.core.windows.net/samples/AzureResourceManager.json)をアップロードします。  **[続行]** をクリックします。  
   
    ![[新しい API エンドポイントへの接続]](./media/customapi-azure-resource-manager-tutorial/createcustom.png)
4. この OpenAPI ファイルは認証に AAD アプリケーションを使用するため、次の画面で、アプリケーションに関する情報をPowerApps に提供する必要があります。  **[クライアント ID]** では、先ほど書き留めておいた AAD の**アプリケーション ID** を入力します。  [クライアント シークレット] では、**キー**を使用します。  最後に、**[リソース URL]** では、「`https://management.core.windows.net/`」と入力します。
   
    > [!IMPORTANT]
> 末尾のスラッシュも含め、リソース URL は上記のとおり正確に入力してください。
   
    ![OAuth 設定](./media/customapi-azure-resource-manager-tutorial/oauthsettings.png)
5. これで、カスタム コネクタが登録され、PowerApps または Microsoft Flow 内で使用できるようになりました。
   
    ![追加されたカスタム コネクタ](./media/customapi-azure-resource-manager-tutorial/createdcustomapi.png)
   
    > [!NOTE]
> サンプル OpenAPI には、すべての ARM 操作が定義されているわけではなく、現在は[すべてのサブスクリプションの一覧表示](https://msdn.microsoft.com/library/azure/dn790531.aspx)操作のみが含まれています。  この OpenAPI ファイルを編集するか、[オンライン OpenAPI エディター](http://editor.swagger.io/)を使用して別の OpenAPI ファイルを作成できます。 このプロセスは、AAD を使用して認証された任意の RESTful API へのアクセスに使用できます。

## <a name="next-steps"></a>次の手順
アプリの作成方法の詳細については、[データからのアプリの作成](get-started-create-from-data.md)に関するページを参照してください。

アプリでフローを使用する方法については、「[Start a flow in an app (アプリでのフローの開始)](using-logic-flows.md)」を参照してください。

カスタム コネクタに関する質問やコメントを投稿するには、[コミュニティに参加](https://aka.ms/powerapps-community)してください。

