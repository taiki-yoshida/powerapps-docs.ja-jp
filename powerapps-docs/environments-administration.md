---
title: "環境の管理 | Microsoft Docs"
description: "環境の作成、名前の変更、削除、セキュリティなどを含む、PowerApps での環境の管理"
services: 
suite: powerapps
documentationcenter: na
author: jamesol-msft
manager: anneta
editor: 
tags: 
ms.service: powerapps
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 01/11/2017
ms.author: jamesol
ms.openlocfilehash: f26c97681a4af40e042d1c943e108a424861f810
ms.sourcegitcommit: 6afca7cb4234d3a60111c5950e7855106ff97e56
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2018
---
# <a name="environments-administration-in-powerapps"></a>PowerApps での環境の管理
[PowerApps 管理センター][1]では、作成した環境および Environment Admin ロールが付与されている環境を管理します。 管理センターから、次の管理操作を実行できます。

* 環境を作成する。
* 環境の名前を変更する。
* Environment Admin ロールまたは Environment Maker ロールのいずれかからユーザーまたはグループを追加または削除する。
* 環境に Common Data Service データベースをプロビジョニングする。
* データ損失防止ポリシーを設定する。
* データベースのセキュリティ ポリシーを設定する (オープン ポリシーまたは制限付きポリシー)。
* Azure AD テナントのグローバル管理者ロールのメンバー (Office 365 のグローバル管理者を含む) も、テナントに作成したすべての環境を管理し、テナント全体のポリシーを設定できます。

## <a name="access-the-powerapps-admin-center"></a>PowerApps 管理センターにアクセスする
PowerApps 管理センターにアクセスするには、次のいずれかを行います。

* [admin.powerapps.com][1] に直接アクセスする。

* [powerapps.com][2] に移動してから、ナビゲーション ヘッダーで歯車アイコンを選択する。
  
    ![](./media/environment-admin/powerapps-gear-dropdown.png)

PowerApps 管理センターで環境を管理するには、次のロールのいずれかが必要です。

* 該当の環境の環境管理者ロール

* Azure AD または Office 365 テナントのグローバル管理者ロール

また、管理センターにアクセスするには PowerApps プラン 2 または Flow プラン 2 が必要です。 詳細については、[PowerApps の価格に関するページ][3]を参照してください。

> [!IMPORTANT]
> PowerApps 管理センターで行う変更はすべて[フロー管理センター][4]に影響し、その反対も同様です。

## <a name="create-an-environment"></a>環境の作成
最初に、**[+ 新しい環境]** をクリックしてダイアログ ボックスを開き、環境を作成します。

![](./media/environment-admin/new-environment-button.png)

次の情報を入力します。

| プロパティ | 説明 |
| --- | --- |
| 環境名 |環境の名前を入力します。 |
| リージョン |環境をホストする場所を選択します。 ユーザーに最も近い場所を使用することをお勧めします。 たとえば、アプリ ユーザーがロンドンにいる場合は、ヨーロッパの場所を選択します。 アプリ ユーザーがニューヨークにいる場合は、米国を選択します。環境がサポートされているリージョンの一覧については、[サポートされているリージョン](regions-overview.md)を参照してください。 |
| この環境のデータベースを作成する |この環境の Common Data Service データベースを作成するには、このチェックボックスを選択します。 データベースは、環境内のすべてのユーザーに開かれるか、データベース ロールによって制限されるようにするかを構成できます。 詳細については、「[Configure database security (データベース セキュリティの構成)](database-security.md)」を参照してください。 |

![](./media/environment-admin/new-environment-updated.png)

最後に、**[環境を作成する]** を選択します。

環境のテーブルに、新しい環境が表示されます。

> [!NOTE]
> 環境を作成すると、作成者はその環境の環境管理者ロールに自動的に登録されます。
> 
> 

## <a name="view-your-environments"></a>環境を表示する
管理センターを開くと、既定で [環境] タブが表示され、お客様が環境管理者である環境が (下図のように) すべて一覧表示されます。

![](./media/environment-admin/environment-list-updated.png)

お客様が Azure AD のグローバル管理者ロールのメンバーまたは Office 365 テナントである場合、自動的にテナント内でユーザーが作成したすべての環境の環境管理者となるため、これらの環境がすべて表示されます。

## <a name="rename-your-environment"></a>環境の名前を変更する
1. [PowerApps 管理センター][1]を開き、一覧から名前を変更する環境を検索して、その環境をクリックまたはタップします。
   
    ![](./media/environment-admin/environment-list-updated3.png)
2. **[詳細]** をクリックまたはタップします。
   
    ![](./media/environment-admin/environment-rename-details-2.png)
3. **[名前]** テキスト ボックスで、新しい名前を入力してから **[保存]** をクリックまたはタップします。
   
    ![](./media/environment-admin/environment-rename-2.png)

## <a name="delete-your-environment"></a>環境を削除する
1. [PowerApps 管理センター][1]で、削除する環境をクリックまたはタップします。
   
    ![](./media/environment-admin/environment-list-updated3.png)
2. **[詳細]** をクリックまたはタップします。
   
    ![](./media/environment-admin/environment-rename-details-2.png)
3. **[環境の削除]** をクリックまたはタップして、環境を削除します。
   
    ![](./media/environment-admin/delete-environment-2.png)

## <a name="create-a-common-data-service-database-for-an-environment"></a>環境に Common Data Service データベースを作成する
環境にデータベースがない場合、環境管理者は次の手順に従って、[PowerApps 管理センター][1]でデータベースを作成できます。 PowerApps プラン 2 のライセンスを持つユーザーのみが Common Data Service データベースを作成できます。

1. 環境のテーブルで、環境を選択します。
   
    ![](./media/environment-admin/choose-environment-updated.png)
2. **[データベース]** タブを選択します。
3. **[データベースの作成]** を選択します。
   
    ![](./media/environment-admin/database-tab.png)
   
    データベースがプロビジョニングされると、次の確認メッセージが表示されます。
   
    ![](./media/environment-admin/database-tab-success.png)

データベースを作成したら、セキュリティ モデルを選択します。 詳細については、「[Configure database security (データベース セキュリティの構成)](database-security.md)」を参照してください。

## <a name="manage-security-for-your-environments"></a>環境のセキュリティを管理する

### <a name="environment-permissions"></a>環境のアクセス許可
環境では、Azure AD テナント内のユーザーはすべてその環境のユーザーです。 ただし、より高い特権のロールを割り当てるには、ユーザーを特定の環境ロールに追加する必要があります。 環境には、環境内でのアクセス許可を提供する 2 つの組み込みの役割があります。

* **環境管理者**ロールは、環境に対して、次を含むすべての管理操作を実行できます。
  
    * Environment Admin ロールまたは Environment Maker ロールのいずれかからユーザーまたはグループを追加または削除する。
  
    * 環境に Common Data Service データベースをプロビジョニングする。
  
    * 環境内で作成されたすべてのリソースを表示し、管理する。
  
    * データ損失防止ポリシーを設定する。 詳細については、[データ損失防止ポリシー](prevent-data-loss.md)に関するページを参照してください。

* **Environment Maker** ロールは、アプリ、接続、カスタム コネクタ、ゲートウェイ、および Microsoft Flow を使用するフローなど、環境内のリソースを作成できます。 環境作成者は、環境で構築したアプリを組織内の他のユーザーに配布することもできます。 個々 のユーザー、セキュリティ グループ、または組織内のすべてのユーザーとアプリを共有できます。 詳細については、[PowerApps でのアプリの共有](share-app.md)に関するページを参照してください。

環境ロールにユーザーまたはセキュリティ グループを割り当てるために、環境管理者は次の手順を [PowerApps 管理センター][1]で実行できます。

1. 環境のテーブルで、環境を選択します。
   
    ![](./media/environment-admin/choose-environment-updated.png)
2. **[セキュリティ]** タブで **[環境ロール]** を選択します。
3. **環境管理者**ロールまたは**環境作成者**ロールのいずれかを選択します。
   
    ![](./media/environment-admin/choose-environment-role.png)
4. Azure Active Directory 内の 1 人以上のユーザーまたは 1 つ以上のセキュリティ グループの名前を指定します。または、組織全体を追加することを指定します。
   
    ![](./media/environment-admin/enter-name.png)
5. **[保存]** を選択して環境ロールに対して割り当てを更新します。

ユーザーまたはグループのすべてのアクセス許可を削除するには、該当するユーザーまたはグループについて、**[x]** アイコンをクリックするかタップします。

> [!NOTE]
> これらの環境のロールに割り当てられているユーザーまたはグループには、環境のデータベース (存在する場合) へのアクセス権が自動的に付与されるわけではありません。データベース所有者が個別にアクセス権を付与する必要があります。 詳細については、「[Configure database security (データベース セキュリティの構成)](database-security.md)」を参照してください。  
> 
> 

### <a name="database-security"></a>データベース セキュリティ
データベース スキーマを作成および変更し、環境内でプロビジョニングされてデータベース内で格納されているデータに接続するための機能は、データベースのユーザー ロールとアクセス許可セットによって制御されます。 環境のデータベース向けのユーザー ロールおよびアクセス許可セットは、**[セキュリティ]** タブの **[ユーザー ロール]** セクションおよび **[アクセス許可セット]** セクションから管理できます。詳細については、「[Configure database security (データベース セキュリティの構成)](database-security.md)」を参照してください。

![](./media/environment-admin/database-security.png)

> [!NOTE]
> 環境管理者には、環境のデータベースのユーザー ロールとアクセス許可セットを作成および管理するためのアクセス権がありません。 この権限は、**データベース所有者**ユーザー ロールのメンバーに限定されています。  
> 
> 

## <a name="data-policies"></a>データ ポリシー
アクセス権のない対象ユーザーと共有されないように、組織のデータを保護する必要があります。 このデータを保護するために、どのコンシューマー サービス/コネクタ固有のビジネス データを共有できるかを定義するポリシーを作成して適用することができます。 データの共有方法を定義するポリシーは、データ損失防止 (DLP) ポリシーと呼ばれます。 環境の DLP ポリシーは、[PowerApps 管理センター][1]の **[データ ポリシー]** セクションで管理できます。  詳細については、[データ損失防止ポリシー](prevent-data-loss.md)に関するページを参照してください。

![](./media/environment-admin/data-policies.png)

## <a name="frequently-asked-questions"></a>よく寄せられる質問
### <a name="how-many-environments-can-i-create"></a>環境はいくつ作成できますか。
各ユーザーは、最大で 2 つの環境を作成できます。

### <a name="how-many-databases-can-i-provision"></a>データベースはいくつプロビジョニングできますか。
各ユーザーは、最大で 2 つのデータベースをプロビジョニングできます。

### <a name="can-i-rename-an-environment"></a>環境の名前は変更できますか。
はい、この機能は、PowerApps 管理センターから使用できます。 詳細については、[環境の管理](environments-administration.md#rename-your-environment)に関するページをご覧ください。

### <a name="can-i-delete-an-environment"></a>環境を削除することはできますか。
はい、この機能は、PowerApps 管理センターから使用できます。 詳細については、[環境の管理](environments-administration.md#delete-your-environment)に関するページをご覧ください。

### <a name="as-an-environment-admin-can-i-view-and-manage-all-resources-apps-flows-apis-etc-for-an-environment"></a>環境管理者として、環境のすべてのリソース (アプリ、フロー、API など) を表示および管理することはできますか。
はい、アプリと環境のフローを表示する機能は、PowerApps 管理センターから使用できます。 詳細については、[アプリの表示](admin-view-apps.md)に関するページをご覧ください。

### <a name="which-license-includes-common-data-service"></a>Common Data Service は、どのライセンスに含まれますか。
PowerApps プラン 2 に含まれます。  このライセンスを含むすべてのプランに関する詳細については、[PowerApps の価格ページ][3]を参照してください。

### <a name="can-the-common-data-service-be-used-outside-of-an-environment"></a>Common Data Service は、環境の外部でも使用できますか。
いいえ。 Common Data Service には環境が必要です。

<!--Reference links in article-->
[1]: https://admin.powerapps.com
[2]: https://web.powerapps.com
[3]: https://powerapps.microsoft.com/pricing/
[4]: https://admin.flow.microsoft.com
