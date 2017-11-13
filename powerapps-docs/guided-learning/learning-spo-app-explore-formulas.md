---
title: "アプリの数式の詳細 (SharePoint リスト) | Microsoft Docs"
description: "数式を使用してアプリの動作をさらにカスタマイズします"
services: 
suite: powerapps
documentationcenter: na
author: mgblythe
manager: anneta
editor: 
tags: 
featuredvideoid: 9TBA19YU7EA
courseduration: 9m
ms.service: powerapps
ms.devlang: na
ms.topic: get-started-article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 12/09/2016
ms.author: mblythe
ms.openlocfilehash: d8ceb2740c95223740e110535fc0c8a1f6f01ae5
ms.sourcegitcommit: 43be6a4e08849d522aabb6f767a81c092419babc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2017
---
# <a name="explore-app-formulas-sharepoint-list"></a>アプリの数式の詳細 (SharePoint リスト)
PowerApps の主な利点の 1 つは従来のアプリケーション コードを記述する必要がないことです。開発者でなくてもアプリを作成できるということです。 とはいえ、アプリのロジックを表現して、アプリのナビゲーション、フィルター処理、並べ替えなどの機能を制御する方法は必要です。 そのために数式が取り入れられています。 Excel の数式を使用したことがあれば、PowerApps のアプローチは理解しやすいでしょう。 このトピックでは、テキストを書式設定する基本的な数式をいくつか示してから、PowerApps が生成されたアプリに含める数式を 3 つ説明します。 数式が実行できる内容を体験しましょう。 時間をとって、生成されたアプリに含まれる他の数式をいくつか確認した後で、ご自分の数式を作成してみてください。

## <a name="understanding-formulas-and-properties"></a>数式とプロパティの詳細
前のトピックで、[Price]\(価格) フィールドをブラウズ画面のギャラリーに含めましたが、通貨記号が表示されず、数字だけが表示されました。 ドル記号を追加し、品目の価格に応じてテキストの色を変更することにします (たとえば、$5 より高い場合は赤、それ以外は緑にします)。 次の図に、考え方を示します。

![色と通貨のテキストの書式設定](./media/learning-spo-app-explore-formulas/text-formatting.png)

通貨の書式設定から始めましょう。 既定では、PowerApps は各品目の Price (価格) の値だけを取得します。この動作は、価格を表示するラベルの **Text** *プロパティ*として設定されています。

![Price (価格) の既定の書式設定](./media/learning-spo-app-explore-formulas/price-default.png)

米国の通貨記号を追加するには、ラベル コントロールをクリックまたはタップして、数式バーで **Text** プロパティを次の数式に設定します。

![Price (価格) の通貨の書式設定](./media/learning-spo-app-explore-formulas/price-formatted.png)

数式 `Text(Price, "[$-en-US]$ ##.00"` では、**Text** *関数*を使用して、数値を書式設定する方法を指定しています。 数式は Excel の数式のようですが、PowerApps の数式はスプレッドシート内のセルではなくコントロールおよびその他のアプリの要素を参照します。 コントロールをクリックまたはタップして、プロパティのドロップダウン リストをクリックまたはタップすると、コントロールに関連するプロパティのリストが表示されます。 たとえば、これはラベルのプロパティのリストの一部です。 さまざまなコントロールに関連するプロパティもあれば、特定のコントロールにしか関連しないコントロールもあります。

![プロパティの設定](./media/learning-spo-app-explore-formulas/properties.png)

価格に基づいて条件付きで色を書式設定するには、ラベルの **Color** プロパティに次のような数式を使用します。`If(Price > 5, Color.Red, Color.Green)`

![Price (価格) の色の書式設定](./media/learning-spo-app-explore-formulas/color-formatted.png)

## <a name="formulas-included-in-the-generated-app"></a>生成されたアプリに含まれる数式
プロパティと組み合わせて数式を使用する方法を理解したところで、生成されたアプリで PowerApps が使用する数式の例を 3 つ紹介します。 例はすべてブラウズ画面の数式で、OnSelect プロパティで動作します。OnSelect プロパティは、ユーザーがアプリのコントロールをクリックまたはタップしたときの動作を定義します。

* 最初の数式は **IconNewItem1** コントロール: ![新しい項目アイコン](./media/learning-spo-app-explore-formulas/icon-add-item.png) に関連付けられています。 このコントロールをクリックまたはタップして、ブラウズ画面から編集/作成画面に移動して項目を作成します。 
  
  * 数式は `NewForm(EditForm1);Navigate(EditScreen1, ScreenTransition.None)` です。
  * この数式は、新しい編集フォームを*インスタンス化*してから、新しい項目を作成できるように編集/作成画面に移動します。 `ScreenTransition.None` という値は、画面間の遷移 (フェードなど) がないことを意味します。
* 2 番目の数式は **IconSortUpDown1** コントロール: ![並べ替えギャラリー アイコン](./media/learning-spo-app-explore-formulas/icon-sort.png) に関連付けられています。 このコントロールをクリックまたはタップして、ブラウズ画面ギャラリーの項目リストを並べ替えます。
  
  * 数式は `UpdateContext({SortDescending1: !SortDescending1})` です。
  * この数式は、`UpdateContext` を使用して `SortDescending1` という*変数*を更新します。 変数の値によって、コントロールをクリックしたときの移動の方向が切り替わります。 これにより、この画面のギャラリーに、項目をどう並べ替えるかが指示されます (詳細はビデオをご覧ください)。 
* 3 番目の数式は **NextArrow1** コントロール: ![詳細に移動矢印アイコン](./media/learning-spo-app-explore-formulas/icon-arrow.png) に関連付けられています。 このコントロールをクリックまたはタップして、ブラウズ画面から詳細画面に移動します。
  
  * 数式は `Navigate(DetailScreen1, ScreenTransition.None)` です。
  * この数式は、詳細画面に移動します。ここでも遷移はありません。

アプリには他にも多くの数式があります。コントロールをクリックして、設定どのような数式がさまざまなプロパティに設定されているか確認してみてください。

## <a name="wrapping-it-all-up"></a>まとめ
ここまで、生成されたアプリおよび、アプリの機能を実現している画面、コントロール、プロパティ、数式の仕組みを概観しました。 ここまで学習を進めてきたら、生成されたアプリのしくみをよく理解できたはずです。 今度は、この理解をご自分のアプリ作成に応用してください。 

次のセクションに進む前に、SharePoint を振り返って、アプリにリスト エクスペリエンスがどのように統合されたか確認しましょう。 ご覧のとおり、**FlooringApp** はリストの*ビュー*として機能するようになりました。アプリは **[Open]** (開く) をクリックすると起動します。 これにより、使いやすくカスタマイズされたエクスペリエンスでリストを簡単に管理できるようになりました。

![Sharepoint リストのビューとしてのアプリ](./media/learning-spo-app-explore-formulas/list-view.png)

これで SharePoint のアプリ セクションが終了しました。ここからは学習内容をお選びいただけます。

* [アプリの管理](learning-manage-share-apps.md)
* [Common Data Service からのアプリの作成とカスタマイズ](learning-case-app-generate.md)

管理のセクションでは、アプリを共有しバージョン管理する方法を示し、アプリ、データ、およびその他のリソースのコンテナーとなる環境について説明します。 管理のセクションには、ある時点ですべての方が目を通すことをお勧めしますが、Common Data Service のセクションにもアプリのカスタマイズの詳細など多くの情報があります。 

