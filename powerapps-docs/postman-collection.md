---
title: "Postman でのカスタム コネクタの説明 | Microsoft Docs"
description: "カスタム コネクタの登録用に Postman Collection を作成します"
services: 
suite: powerapps
documentationcenter: 
author: archnair
manager: anneta
editor: 
ms.service: powerapps
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/28/2017
ms.author: archanan
ms.openlocfilehash: fd060ff873ee376b7ca886f721d360372c1d13ed
ms.sourcegitcommit: 43be6a4e08849d522aabb6f767a81c092419babc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2017
---
# <a name="describe-a-custom-connector-with-postman"></a>Postman でのカスタム コネクタの説明
[Postman](https://www.getpostman.com/) は、API 開発をより迅速で簡単にするためのツールです。 このチュートリアルでは、Postman Collection を作成して、PowerApps 内の[カスタム コネクタ](register-custom-api.md)を簡単に作成できるようにする方法について説明します。

## <a name="prerequisites"></a>前提条件
* [Postman アプリ](https://www.getpostman.com/apps)のインストールします

## <a name="create-a-postman-collection"></a>Postman Collection の作成
Azure Cognitive Services の [Text Analytics API](https://www.microsoft.com/cognitive-services/en-us/text-analytics-api) 用の Postman Collection を作成しましょう。 この API は、渡されたテキスト内の言語、センチメント、キー フレーズを識別します。

1. Postman Collection を作成するための最初のステップは、要求を作成することです。 要求を作成する際には、HTTP 動詞、要求 URL、クエリまたはパスのパラメーター、ヘッダー、および本文を設定できます。 詳しくは、Postman のドキュメントで[要求の送信](https://www.getpostman.com/docs/requests)に関するトピックを参照してください。 Detect Language API エンドポイントについては、次のように値を設定します。
   
    ![Postman の要求](./media/postman-collection/request.png)
   
    パラメーターの詳細と使用される値:
   
   | パラメーター | 値 |
   | --- | --- |
   | 動詞 |POST |
   | 要求 URL |https://westus.api.cognitive.microsoft.com/text/analytics/v2.0/languages |
   | パラメーター |numberOfLanguagesToDetect |
   | 認証 |“No Auth” |
   | ヘッダー |Ocp-Apim-Subscription-Key = <your subscription key> <br/>Content-Type = application/json |
   | 本文 |<code>{<br/>&nbsp;&nbsp;&nbsp;"documents": [<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"id": "1",<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"text": "Hello World"<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}<br/>&nbsp;&nbsp;]<br/>}<code> |
2. **[Send]** (送信) をクリックして要求を作成し、応答を取得します。
3. **[Save]** (保存) をクリックして、Postman Collection に要求を保存します。
   
    ![Postman の応答](./media/postman-collection/request-response-save.png)
4. **[Save Request]** (要求の保存) ダイアログ ボックスで、**[Request name]** (要求名) と **[Request description]** (要求の説明) を入力します。 これらの値はカスタム コネクタで使用します。
   
    ![Postman でのコレクションの保存](./media/postman-collection/save-request-note.png)
   
    要求に対する応答を保存することもできます。 現在、カスタム コネクタでは要求ごとに 1 つの応答しかサポートされていません。 要求ごとに複数の応答を保存した場合は、最初の 1 つだけが使用されます。
   
    ![Postman での応答の保存](./media/postman-collection/save-response.png)
5. その他の要求と応答を作成して保存し、Postman Collection の作成を続行します。
6. すべての要求と応答について Postman Collection の作成が完了したら、そのコレクションをエクスポートします。
   
    ![Postman でのエクスポート](./media/postman-collection/export.png)
7. エクスポート形式として、**[Collection v1]** (コレクション v1) を選択します。
   
    ![Postman でのエクスポート](./media/postman-collection/export2.png)

これで、Postman Collection を使用して PowerApps のカスタム コネクタを作成できるようになりました。 詳しくは、「[PowerApps でのカスタム コネクタの登録と使用](register-custom-api.md)」をご覧ください。 

