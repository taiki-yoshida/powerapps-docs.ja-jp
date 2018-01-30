---
title: "API コネクタを開発する | Microsoft Docs"
description: "API を記述し、認証の種類を指定し、トリガーとアクションを作成し、テストを行います。"
services: 
suite: powerapps
documentationcenter: na
author: asavaritayal
manager: anneta
editor: 
tags: 
ms.service: powerapps
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/06/2017
ms.author: astay
ms.openlocfilehash: 68a0be6c6be91ff5b89b3e06aecc242f987a4cf4
ms.sourcegitcommit: 33099e6197c0139679cd08c42e9e2a5717904c92
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/12/2018
---
# <a name="develop-an-api-connector-powerapps"></a>API コネクタを開発する (PowerApps)
コネクタを作成するプロセスには、複数の手順が含まれています。 最初に、[PowerApps](https://web.powerapps.com/) で、ページの右上隅にある **[設定]** ボタン (歯車のアイコン) をクリックするかタップします。 次に、**[カスタム コネクタ]** をクリックするかタップします。

![API コネクタの検索](./media/api-connectors-dev/finding-custom-apis.png)

## <a name="describe-your-api"></a>API を記述する
API コネクタは、HTTP API のインターフェイスを定義するための [OpenAPI 標準](https://swagger.io/)を使用して記述します。 既存の OpenAPI ファイルを使用して作成を開始できます。または、[Postman コレクション](https://www.getpostman.com/docs/collections)をインポートできます (OpenAPI ファイルは自動生成されます)。 

![API 定義図](./media/api-connectors-dev/build-your-api-updated.png)

これらの API 記述のどちらから始めた場合でも、ウィザードのメタデータ フィールドは自動的に入力されます。 これらはいつでも編集できます。  

## <a name="build-security"></a>セキュリティを設定する
サービスでサポートされる認証の種類を選択し、ID がサービスとクライアント間を適切にフローできるようにするための詳詳細情報を指定します。 

![セキュリティ図](./media/api-connectors-dev/security.png)

詳細については、[コネクタのセキュリティ](register-custom-api.md)に関するページを参照してください。

## <a name="build-triggers-and-actions"></a>トリガーとアクションを作成する
1. コネクタのトリガーとアクションを作成するには、**[定義]** タブに切り替えます。 
   
    ![定義図](./media/api-connectors-dev/definition.png)
2. ウィザードを使用して、新しい操作を追加するか、既存の操作のスキーマと応答を編集できます。 各操作の **[全般]** のプロパティを使用して、コネクタのエンド ユーザー エクスペリエンスを制御できます。 さまざまな種類の操作の詳細については、次のリンクを参照してください。
   
   * [トリガー](https://flow.microsoft.com/documentation/customapi-webhooks) (PowerApps では表示されません)
   * [アクション](register-custom-api.md)
     
     Microsoft Flow 向けの高度な機能を実装するには、[API コネクタ用の OpenAPI 拡張](https://flow.microsoft.com/documentation/customapi-how-to-swagger/)に関するページを参照してください。 
3. 最後に、**[コネクタの作成]** をクリックするかタップして、API コネクタを登録します。

ウィザードで利用できないその他の機能については、[ condevhelp@microsoft.com](mailto:condevhelp@microsoft.com) にお問い合わせください。

## <a name="test-the-connector"></a>コネクタをテストする
送信する前に、1 つまたは複数の方法で、作成した API コネクタをテストします。 

* API コネクタ [テスト ウィザード](https://flow.microsoft.com/blog/new-updates-custom-api/)を使用して、各操作を呼び出してその機能と応答スキーマを検証できます。
* Microsoft Flow 用のデザイナーで、作成した API コネクタを使用して、フローを視覚的に構築できます。 このテスト方法では、コネクタのユーザー インターフェイス機能とその他の機能を視覚化できます。
* PowerApps Studio で、数式バーを使用して各操作を呼び出し、応答を画面上のコントロールにバインドできます。

このトピックでは概要を説明しました。詳細については、[カスタム API の登録と使用](register-custom-api.md)に関するページを参照してください。

