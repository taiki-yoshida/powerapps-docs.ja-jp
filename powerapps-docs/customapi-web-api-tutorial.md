---
title: "Web API 用カスタム コネクタの構築 | Microsoft Docs"
description: "PowerApps で Azure Active Directory 認証を使用する ASP.NET Web API を作成する方法について説明します。"
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
ms.date: 10/26/2016
ms.author: mblythe
ms.openlocfilehash: 4fc9fb1d183ec910d37383be6629aaa67cf3723d
ms.sourcegitcommit: 68eee592c351688e5d0bd458f33a70be507fa53f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2018
---
# <a name="build-a-custom-connector-for-a-web-api-in-powerapps"></a>Web API 用カスタム コネクタの構築
このチュートリアルでは、ASP.NET Web API の構築を開始して Azure Web Apps でホストし、Azure Active Directory 認証を有効にした後、PowerApps に ASP.NET Web API を登録する方法について説明します。 API を登録すると、API に接続して、アプリから API を呼び出すことができます。

## <a name="prerequisites"></a>前提条件
* [Azure サブスクリプション](https://azure.microsoft.com/en-us/free/)。
* [PowerApps アカウント](https://powerapps.microsoft.com)。
* [Visual Studio](https://www.visualstudio.com/vs/) 2013 以降。

## <a name="create-an-aspnet-web-api-and-deploy-it-to-azure"></a>ASP.NET Web API を作成して Azure にデプロイする
1. Visual Studio で、**[ファイル]** > **[新しいプロジェクト]** の順にクリックし、新しい C# ASP.NET Web アプリケーションを作成します。
   
    ![新しい Web アプリ](./media/customapi-web-api-tutorial/newwebapp.png)
2. **[Web API]** テンプレートを選択します。  **[クラウドにホストする]** チェック ボックスはオンのままにします。  **[認証の変更]** をクリックします。
   
    ![新しい Web プロジェクト テンプレート](./media/customapi-web-api-tutorial/new-web-api.png)
3. **[認証なし]** を選択し、**[OK]** をクリックします。
   
    ![[認証なし]](./media/customapi-web-api-tutorial/noauth.png)
4. **[新しい ASP.NET プロジェクト]** ダイアログで **[OK]** をクリックします。  [Microsoft Azure Web App の構成] ダイアログが表示されます。
   
    ![[Microsoft Azure Web App の構成]](./media/customapi-web-api-tutorial/azure-publishing.png)]
   
    Azure アカウントを選択し、**Web アプリ名**を入力 (または既定値のままに) して、Azure **サブスクリプション**を選択します。  **App Service プラン** (サブスクリプション内の Web アプリのコレクション) を選択または作成します。  **リソース グループ** (サブスクリプション内の Azure リソースのグループ) を選択または作成します。  Web アプリをデプロイするリージョンを選択します。  Web API で必要な場合は、Azure の**データベース サーバー**を選択または作成します。  最後に、**[OK]** をクリックします。
5. Web API を構築します。
   
    > [!NOTE]
> Web API 用のコードがまだ準備できていない場合は、チュートリアル「[Getting Started with ASP.NET Web API 2 (C#)](http://www.asp.net/web-api/overview/getting-started-with-aspnet-web-api/tutorial-your-first-web-api)」 (ASP.NET Web API 2 (C#) の使用を開始) を実行してください。
6. Web API を PowerApps に接続するには、その操作が記述された [OpenAPI](http://swagger.io/) ファイルが必要です。  [オンライン エディター](http://editor.swagger.io/)を使用して独自の OpenAPI を作成することもできますが、このチュートリアルでは、[Swashbuckle](https://github.com/domaindrivendev/Swashbuckle/blob/master/README.md) というオープンソースのツールを使用します。  Visual Studio プロジェクトに Swashbuckle Nuget パッケージをインストールするには、**[ツール]** > **[NuGet パッケージ マネージャー]** > **[パッケージ マネージャー コンソール]** の順にクリックし、パッケージ マネージャー コンソールで `Install-Package Swashbuckle` コマンドを入力します。
   
    ![Install-Package Swashbuckle](./media/customapi-web-api-tutorial/swashbuckle-console.png)
   
    > [!TIP]
> Swashbuckle のインストール後に Web API アプリケーションを実行すると、URL `http://<your root URL>/swagger/docs/v1` に OpenAPI ファイルが生成されます。  生成されたユーザー インターフェイスは `http://<your root URL>/swagger` でも利用できます。
7. Web API の準備ができたら、Azure に発行します。 Visual Studio から発行するには、ソリューション エクスプローラーで Web プロジェクトを右クリックし、**[発行]** をクリックして、[発行] ダイアログ ボックスの指示に従います。
8. `https://<azure-webapp-url>/swagger/docs/v1` に移動して OpenAPI JSON を取得します。  内容を JSON ファイルとして保存します。  ブラウザーによっては、テキストをコピーして空のテキスト ファイルに貼り付けることが必要になる場合があります。   
   
    > [!IMPORTANT]
> 重複する操作 ID を持つ OpenAPI ドキュメントは無効です。 サンプル C# テンプレートを使用している場合、操作 ID `Values_Get` が 2 回繰り返されています。 これを修正するには、一方のインスタンスを `Value_Get` に変更してから再発行します。 このチュートリアルで[サンプルの OpenAPI ファイル](http://pwrappssamples.blob.core.windows.net/samples/webAPI.json)をダウンロードすることもできます。 使用する前に、(`//` で始まる) コメントを必ず削除してください。

## <a name="set-up-azure-active-directory-authentication"></a>Azure Active Directory 認証を設定する
ここでは、2 つの Azure Active Directory (AAD) アプリケーションを Azure に作成します。  この方法の例については、[Azure Resource Manager のチュートリアル](customapi-azure-resource-manager-tutorial.md#enable-authentication-in-azure-active-directory)を参照してください。

> [!IMPORTANT]
> 両方のアプリが同じディレクトリに含まれている必要があります。

### <a name="first-aad-application-securing-the-web-api"></a>1 つ目の AAD アプリケーション: Web API のセキュリティ保護
1 つ目の AAD アプリケーションは、Web API のセキュリティ保護に使用されます。 **webAPI** という名前を付けます。  次の値を使用して、前述のリンク先のチュートリアルの手順 (「*Azure Active Directory で認証を有効にする」) に従います。

* サインオン URL: `https://login.windows.net`
* 応答 URL: `https://<your-root-url>/.auth/login/aad/callback`
* クライアント キーは必要ありません。
* アクセス許可を委任する必要はありません。

> [!IMPORTANT]
> アプリケーション ID をメモしておいてください。  これは後で必要になります。

### <a name="second-aad-application-securing-the-custom-connector-and-delegated-access"></a>2 つ目の AAD アプリケーション: カスタム コネクタのセキュリティ保護と委任されたアクセス
2 つ目の AAD アプリケーションは、カスタム コネクタの登録をセキュリティで保護し、1 つ目のアプリケーションで保護された Web API への委任されたアクセスを取得するために使用します。 このアプリケーションに **webAPI-customAPI** という名前を付けます。

* サインオン URL: `https://login.windows.net`
* 応答 URL: `https://msmanaged-na.consent.azure-apim.net/redirect`
* Web API への委任されたアクセスを取得するためのアクセス許可を追加します。
* このアプリケーションのアプリケーション ID も後で必要となるため、メモしておきます。
* クライアント キーを生成し、それを安全な場所に保存します。 このキーは後で必要になります。

## <a name="add-authentication-to-your-azure-web-app"></a>Azure Web アプリに認証を追加する

1. [Azure Portal](https://portal.azure.com) にサインインし、最初のセクションでデプロイした Web アプリを見つけます。

2. **[設定]** をクリックして、**[認証/承認]** を選択します。

3. **[App Service 認証]** をオンにし、**[Azure Active Directory]** を選択します。  次のブレードで、**[Express]** を選択します。  

4. **[既存の AD アプリを選択する]** をクリックし、前に作成した **webAPI** AAD アプリケーションを選択します。

これで、AAD を使用して Web アプリケーションを認証できるようになります。

## <a name="add-the-custom-connector-to-powerapps"></a>PowerApps にカスタム コネクタを追加する
1. Web アプリに使用される `securityDefintions` オブジェクトと AAD 認証を追加するように OpenAPI ファイルを変更します。 OpenAPI ファイルの **host** プロパティを含むセクションは次のようになります。

    ```javascript
    // File header should be above here...

    "host": "<your-root-url>",
    "schemes": [
        "https"         //Make sure this is https!
    ],
    "securityDefinitions": {
        "AAD": {
            "type": "oauth2",
            "flow": "implicit",
            "authorizationUrl": "https://login.windows.net/common/oauth2/authorize",
            "scopes": {}
        }
    },

    // The rest of the OpenAPI document follows...
    ```

2. [PowerApps](https://web.powerapps.com) にブラウザーでアクセスし、カスタム コネクタを [PowerApps でのカスタム コネクタの登録と使用](register-custom-api.md)に関する説明に従って追加します。

3. OpenAPI ファイルのアップロードが完了すると、ウィザードでは、Web API に AAD 認証が使用されていることが自動的に検出されます。

4. カスタム コネクタの AAD 認証を構成します。  
   
   * **クライアント ID**: "*webAPI-CustomAPI のクライアント ID*"
   * **シークレット**: "*webAPI-CustomAPI のクライアント キー*"
   * **ログイン URL**: `https://login.windows.net`
   * **ResourceUri**: "*webAPI のクライアント ID*"
5. **[作成]** をクリックし、カスタム コネクタへの接続を作成します。

## <a name="next-steps"></a>次のステップ
[Azure Resource Manager カスタム コネクタ チュートリアル](customapi-azure-resource-manager-tutorial.md)を実行します。

