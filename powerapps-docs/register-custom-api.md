---
title: "カスタム コネクタの登録と使用 | Microsoft Docs"
description: "OpenAPI と Postman を使用して、PowerApps でカスタム コネクタを登録および使用します。"
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
ms.date: 05/05/2017
ms.author: mblythe
ms.openlocfilehash: 2eac422675fc8741848ab90777824a10ec9e0e1e
ms.sourcegitcommit: 6afca7cb4234d3a60111c5950e7855106ff97e56
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2018
---
# <a name="register-and-use-custom-connectors-in-powerapps"></a>PowerApps でのカスタム コネクタの登録と使用
PowerApps では、従来のアプリケーション コードをまったく使用せずに、完全な機能を備えたアプリを作成できます。 しかし、PowerApps の機能を拡張する必要があり、そのためには Web サービスを使用するのが自然な場合もあります。 アプリはサービスに接続し、操作を実行し、データを取得することができます。 PowerApps で接続したい Web サービスがある場合は、そのサービスをカスタム コネクタとして登録できます。 このプロセスにより、PowerApps は Web API の特性 (必要な認証、サポートする操作、各操作のパラメーターと出力など) を把握できます。

このトピックでは、カスタム コネクタの登録と使用に必要な手順を説明し、例として Azure Cognitive Services の [Text Analytics API](https://www.microsoft.com/cognitive-services/en-us/text-analytics-api) を使用します。 この API は、渡されたテキスト内の言語、センチメント、キー フレーズを識別します。 次の図に、サービス、サービスから作成するカスタム コネクタ、API を呼び出すアプリの間の相互関係を示します。

![API、カスタム コネクタ、およびアプリ](./media/register-custom-api/intro-graphic.png)

## <a name="prerequisites"></a>前提条件
* [PowerApps アカウント](https://powerapps.microsoft.com)。
* JSON 形式の OpenAPI ファイル、OpenAPI 定義の URL、または API の Postman Collection。 いずれもない場合については、後で説明します。
* カスタム コネクタのアイコンとして使用する画像 (省略可能)。

## <a name="steps-in-the-custom-connector-process"></a>カスタム コネクタのプロセスに含まれる手順
カスタム コネクタのプロセスにはいくつかの手順があります。以下で、それらの手順について簡単に説明します。 この記事では何らかの種類の認証済みアクセスが設定された RESTful API が既にあることを前提としているため、この記事の残りの部分では手順 3 ～ 6 について重点的に説明します。 手順 1 と 2 の例については、「[PowerApps 用のカスタム Web API の作成](customapi-web-api-tutorial.md)」をご覧ください。

1. 任意の言語とプラットフォームで **RESTful API を作成**します。 Microsoft のテクノロジに関しては、次のいずれかをお勧めします。
   
   * Azure Functions
   * Azure Web Apps
   * Azure API Apps
2. 次のいずれかの認証機構を使用して、**API をセキュリティで保護**します。 API への非認証アクセスを許可することもできますが、お勧めしません。
   
   * Azure Active Directory。 詳細については、「[PowerApps で Azure Active Directory とカスタム コネクタを使用する](customapi-azure-resource-manager-tutorial.md)」をご覧ください。
   * Dropbox、Facebook、SalesForce などの特定のサービス用の OAuth 2.0
   * 一般的な OAuth 2.0
   * API キー
   * 基本認証
3. 業界標準の 2 つの方法のいずれかで **API を記述**して、PowerApps が API に接続できるようにします。
   
   * OpenAPI ファイル (Swagger ファイルとも呼ばれます) - 手順 4 で登録プロセスの一環として OpenAPI ファイルを作成することもできます。
   * Postman Collection
4. PowerApps のウィザードを使用して、**カスタム コネクタを登録**します。ここで API の説明、セキュリティの詳細、その他の情報を指定します。

5. アプリで**カスタム コネクタを使用**します。 アプリで API への接続を作成し、PowerApps でネイティブ関数を呼び出すのと同じように、API で提供されるすべての操作を呼び出します。

6. **カスタム コネクタを共有**します。これは PowerApps で他のデータ接続に対して行うのと同様です。 この手順は省略可能ですが、通常、複数のアプリ作成者の間でカスタム コネクタを共有するときに役立ちます。

## <a name="describe-your-api"></a>API を記述する
何らかの種類の認証済みアクセスが設定された API が既にある場合、PowerApps がその API に接続できるようにするために、API を記述する方法が必要です。 そのために、OpenAPI ファイルまたは Postman Collection を作成します。これは*任意の* REST API エンドポイントから行うことができます。その例を次に示します。

* 一般公開されている API ([Spotify](https://developer.spotify.com/)、[Uber](https://developer.uber.com/)、[Slack](https://api.slack.com/)、[Rackspace](http://docs.rackspace.com/) など)。
* 独自に作成してクラウド ホスティング プロバイダー (Amazon Web Services (AWS)、Heroku、Google Cloud など) にデプロイする API。
* 自社のネットワークにデプロイされたカスタム基幹業務 API (ただし、その API はパブリック インターネットに公開されていることが必要)。

OpenAPI ファイルと Postman Collection はさまざまな形式を使用しますが、いずれも API の操作とパラメーターを記述する、言語に依存しない、コンピューターが読み取り可能なドキュメントです。

* これらのドキュメントは、API の基盤となっている言語とプラットフォームに応じたさまざまなツールを使用して生成できます。 OpenAPI ファイルの例については、[Text Analytics API のドキュメント](https://westus.dev.cognitive.microsoft.com/docs/services/TextAnalytics.V2.0/export?DocumentFormat=Swagger&ApiName=Azure)をご覧ください。
* API 用の OpenAPI ファイルを持っておらず、作成したくない場合は、Postman Collection を使用してもカスタム コネクタを簡単に作成できます。 詳細については、「[Create a Postman Collection](postman-collection.md)」(Postman Collection の作成) をご覧ください。
* PowerApps は最終的には OpenAPI をバックグラウンドで使用するので、Postman Collection は解析されて OpenAPI 定義ファイルに変換されます。

> [!NOTE]
> ファイルのサイズは 1 MB 未満である必要があります。

### <a name="getting-started-with-openapi-and-postman"></a>OpenAPI と Postman の概要
* OpenAPI を初めて使用する場合は、swagger.io サイトの[OpenAPI の概要](http://swagger.io/getting-started/)に関するページをご覧ください。
* Postman を初めて使用する場合は、Postman のサイトから [Postman アプリ](https://www.getpostman.com/apps)をインストールしてください。
* Azure API Apps または Azure Functions を使用して API が作成されている場合、詳細については、「[Azure でホストされる API を PowerApps と Microsoft Flow にエクスポートする](https://docs.microsoft.com/azure/app-service/app-service-export-api-to-powerapps-and-flow)」をご覧ください。

## <a name="register-your-custom-connector"></a>カスタム コネクタを登録する
OpenAPI ファイルまたは Postman Collection を使用して、PowerApps にカスタム コネクタを登録します。

1. [powerapps.com](https://web.powerapps.com) の左側のメニューで、**[接続]** を選択します。 省略記号 (**...**) を選択し、右上隅の **[Manage custom connectors]** (カスタム コネクタの管理) を選択します。
   
     > [!TIP]
> モバイル ブラウザーでカスタム コネクタを管理する場所が見つからない場合は、左上隅のメニューの下にある可能性があります。
   
    ![カスタム コネクタの作成](./media/register-custom-api/managecustomapi.png)  
2. **[Create custom connector]** (カスタム コネクタの作成) を選択します。
   
    ![カスタム コネクタのプロパティ](./media/register-custom-api/newcustomapi.png)
3. **[全般]** タブで、カスタム コネクタを作成する方法を選択します。
   
   * OpenAPI ファイルをアップロードする

   * OpenAPI URL を使用する

   * Postman Collection V1 をアップロードする
     
     ![カスタム コネクタの作成方法](./media/register-custom-api/choosehowtocreate.png)
     
     カスタム コネクタのアイコンをアップロードします。 [説明]、[ホスト]、[ベース URL] の各フィールドは通常、OpenAPI ファイルからの情報を利用して自動設定されます。 自動設定されなかった場合は、それらのフィールドに情報を追加できます。 **[続行]** を選択します。
4. **[セキュリティ]** タブで、認証プロパティを入力します。
   
    ![認証の種類](./media/register-custom-api/authenticationtypes.png)
   
   * 認証の種類は、OpenAPI の `securityDefinitions` オブジェクトで定義されている内容に基づいて自動設定されます。 OAuth2.0 の例を以下に示します。
     
       ```
       "securityDefinitions": {
           "AAD": {
           "type": "oauth2",
           "flow": "accessCode",
           "authorizationUrl": "https://login.windows.net/common/oauth2/authorize",
           "scopes": {}
           }
       },
       ```
   * OpenAPI ファイルで `securityDefintions` オブジェクトが使用されていない場合は、値を追加する必要はありません。
   * Postman Collection を使用する場合、認証の種類は、サポートされる認証の種類 (OAuth 2.0 や Basic など) を使用している場合にのみ自動設定されます。
   * Azure Active Directory (AAD) 認証の設定の例については、「[PowerApps 用のカスタム Web API の作成](customapi-web-api-tutorial.md#set-up-azure-active-directory-authentication)」をご覧ください。
5. **[定義]** タブで、OpenAPI ファイルまたは Postman Collection に定義されているすべての操作が、要求と応答の値とともに自動設定されます。 必要なすべての操作が定義されている場合は、この画面に変更を加えずに、登録プロセスの手順 6 に進んでください。
   
    ![[定義] タブ](./media/register-custom-api/definitiontab.png)
   
    既存の操作を編集するか、カスタム コネクタに新しい操作を追加する必要がある場合は、以下の説明に従ってください。
   
   1. OpenAPI ファイルまたは Postman Collection に存在しない新しい操作を追加する場合は、左側のウィンドウで **[新しい操作]** を選択し、**[全般]** セクションにその操作の名前、説明、表示設定を入力します。
   2. **[要求]** セクションで、右上の **[サンプルからのインポート]** を選択します。 右側のフォームに、サンプルの要求を貼り付けます。 通常、サンプルの要求は API のドキュメントで提供されています。そこで **[動詞]**、**[要求 URL]**、**[ヘッダー]**、**[本文]** の各フィールドに入力する情報を入手できます。 例については、[Text Analytics API のドキュメント](https://westus.dev.cognitive.microsoft.com/docs/services/TextAnalytics.V2.0/operations/56f30ceeeda5650db055a3c6)をご覧ください。
      
       ![サンプルからのインポート](./media/register-custom-api/importfromsample.png)

   3. **[インポート]** を選択して、要求の定義を完了します。 同様の方法で応答を定義します。
6. すべての操作を定義したら、**[作成]** を選択してカスタム コネクタを作成します。
7. カスタム コネクタの作成が完了したら、**[テスト]** タブに移動して、API で定義されている操作をテストします。 接続を選択し、入力パラメーターを指定して操作をテストします。
   
    ![カスタム コネクタのテスト](./media/register-custom-api/testcustomapi.png)
   
    呼び出しが成功した場合は、有効な応答が返されます。
   
    ![API のテストの応答](./media/register-custom-api/testapiresponse.png)

## <a name="use-your-custom-connector"></a>カスタム コネクタを使用する
API を登録したので、他のデータ ソースの場合と同じようにカスタム コネクタをアプリに追加します。 ここでは、簡単な例を使用して手順を説明します。 データ接続の詳細については、「[PowerApps でデータ接続を追加する](add-data-connection.md)」をご覧ください。

1. PowerApps Studio の右側のウィンドウで、**[データ ソースの追加]** をクリックまたはタップします。
   
    ![](./media/register-custom-api/data-source.png)
2. 作成したカスタム コネクタをクリックまたはタップします。
   
    ![](./media/register-custom-api/connector.png)
3. 接続するサービスへのサインインに必要な手順があれば実行します。 API が OAuth 認証を使用する場合は、サインイン画面が表示されることがあります。 API キー認証の場合は、キーの値を求められることがあります。
4. アプリで API を呼び出します。 ここでは例として、Cognitive Services にテキストを送信し、0 ～ 1 のセンチメント スコアを取得してパーセントで表示するアプリを作成しました。
   
   * このコネクタでは、数式バーに「Az」と入力し始めると、API とその API によって利用できる操作が表示されます。
     
       ![](./media/register-custom-api/formula.png)
   * 呼び出しの全体を以下に示します。この呼び出しでは、`TextInput` コントロールからのテキストを渡し、スコアを取得して、アプリに表示します。
     
       ```
       'AzureMachineLearning-TextAnalytics'.Sentiment({documents:Table({language:"en",id:"1",text:TextInput.Text})}).documents.score)
       ```
   * 返されるデータを処理するためにアプリに少し手を加えますが、それほど複雑ではありません。

完成したアプリは次の図のようになります。 単純なアプリですが、カスタム コネクタから Cognitive Services を呼び出すことで強力な機能が得られました。

![](./media/register-custom-api/finished-app.png)

### <a name="quota-and-throttling"></a>クォータとスロットル
* カスタム コネクタの作成のクォータの詳細については、[PowerApps の価格](https://powerapps.microsoft.com/pricing/)に関するページをご覧ください。 自分に対して共有されているカスタム コネクタは、このクォータにはカウントされません。
* カスタム コネクタに対して作成された各接続について、ユーザーは 1 分間あたり最大 500 件の要求を行うことができます。

## <a name="share-your-custom-connector"></a>カスタム コネクタを共有する
カスタム コネクタを作成したら、組織内の他のユーザーと共有できます。 API を共有すると、他のユーザーはそれに依存する可能性があり、カスタム コネクタを削除すると API へのすべての接続が削除されるという点に注意してください。 組織外のユーザーにコネクタを提供したい場合は、[PowerApps でのカスタム コネクタの認定の概要](api-connector-overview.md)に関する記事をご覧ください。

1. [powerapps.com](https://web.powerapps.com) の左側のメニューで、**[接続]** を選択します。 省略記号 (**...**) を選択し、右上隅の **[Manage custom connectors]** (カスタム コネクタの管理) を選択します。
   
    ![新しい接続](./media/register-custom-api/managecustomapi.png)
2. コネクタの省略記号 (**. . .**) ボタンを選択し、**[プロパティの表示]** を選択します。  
   
    ![コネクタのプロパティの表示](./media/register-custom-api/view-properties.png)
3. カスタム API を選択し、**[共有]** を選択した後、API へのアクセスを許可するユーザーまたはグループを入力します。  
   
    ![カスタム コネクタの共有](./media/register-custom-api/sharecustomapi.png)
4. **[保存]** を選択します。

## <a name="next-steps"></a>次の手順
[Postman Collection の作成方法を確認する](postman-collection.md)。

[ASP.NET Web API を使用する](customapi-web-api-tutorial.md)。

[Azure Resource Manager API を登録する](customapi-azure-resource-manager-tutorial.md)。

