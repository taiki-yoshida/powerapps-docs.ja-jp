---
title: "アプリのカスタマイズ (Common Data Service) | Microsoft Docs"
description: "アプリの画面、コントロール、およびフィールドを更新します"
services: 
suite: powerapps
documentationcenter: na
author: mgblythe
manager: anneta
editor: 
tags: 
featuredvideoid: wHy72cOe8Os
courseduration: 12m
ms.service: powerapps
ms.devlang: na
ms.topic: get-started-article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 12/09/2016
ms.author: mblythe
ms.openlocfilehash: bc5ce767124f531e70c32c34087e0572a87923f2
ms.sourcegitcommit: 43be6a4e08849d522aabb6f767a81c092419babc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2017
---
# <a name="customize-the-app-common-data-service"></a>アプリのカスタマイズ (Common Data Service)
このセクションの最初の 2 つのトピックでは、Common Data Service のエンティティからアプリを生成し、生成したアプリを詳しく確認して 3 画面アプリの構造について学びました。 PowerApps に生成されるアプリは便利ですが、多くの場合は、生成された後でアプリをカスタマイズします。 このトピックでは、アプリのブラウズ画面の変更方法をいくつか説明します。 すべての画面をカスタマイズすることができますが、1 画面に集中して、カスタマイズについて少し詳しく説明します。 エンティティ、Excel ファイル、またはその他のソースから生成した任意のアプリを取り上げ、カスタマイズ方法を確認することをお勧めします。 これが本当にアプリの構造を学習するベストな方法なのです。

## <a name="change-gallery-and-data-bindings"></a>ギャラリーとデータ バインディングを変更する
PowerApps がアプリを生成したときに、使用するレイアウトと各画面に表示する特定のフィールドが決定されました。 このアプリでは、ステータス バーを持つギャラリー コントロールを選択してみましょう (すぐ後でステータス バーをカスタマイズします)。 右側のウィンドウの **[Layout]** (レイアウト) タブで、目的のレイアウトを選択します。 変更と同時に PowerApps がアプリを更新するので、結果はすぐに表示されます。

![ブラウズ画面のレイアウトを変更する](./media/learning-case-app-customize/change-layout.png)

右の基本レイアウトを使用して、表示されるフィールドを変更しましょう。 最初の項目のフィールドをクリックまたはタップして、右側のウィンドウで項目ごとに表示されるデータを変更します。 これにより、エンティティの各項目の概要が分かりやすくなります。

![ブラウズ画面のフィールドを変更する](./media/learning-case-app-customize/change-browse-fields.png)

## <a name="change-the-app-theme"></a>アプリのテーマを変更する
PowerApps には、アプリで使用できる一連のテーマが用意されています。テーマは PowerPoint のものによく似ています。 次の画面では、**Dune** (砂丘) というテーマが適用されていて、アプリに貼り付けたシンプルなロゴが表示されています。 これらは基本的な変更ですが、アプリの外観を改善するためにできることはたくさんあります。 

![テーマを変更してロゴを追加する](./media/learning-case-app-customize/change-theme.png)

## <a name="use-a-formula-to-show-the-case-status"></a>数式を使用してケースの状態を表示する
PowerApps の主な利点の 1 つは従来のアプリケーション コードを記述する必要がないことです。開発者でなくてもアプリを作成できるということです。 とはいえ、アプリのロジックを表現してアプリのナビゲーション、フィルター処理、並べ替えなどの機能を制御する方法は必要です。 そのために数式が取り入れられています。

Excel の数式を使用したことがあれば、PowerApps のアプローチは理解しやすいでしょう。 ケースが解決済みの場合はステータス バーを緑、それ以外の場合は赤にすることにします。 そのためには、画面で状態コントロールを選択して、数式バーでこのコントロールの **Fill** プロパティを次の数式に設定します: `If(Status="Resolved", Color.Green, Color.Red)`。 Excel の数式のようですが、PowerApps の数式はスプレッドシート内のセルではなくコントロールとその他のアプリの各要素を参照します。 下図に、数式を設定する場所とアプリでの結果を示します。

![ケースの状態を表示する数式](./media/learning-case-app-customize/case-status.png)

## <a name="sort-and-filter-based-on-date"></a>日付に基づいて並べ替えフィルター処理する
生成されたアプリのブラウズ画面では、ケースを検索し、ギャラリー内の項目リストを並べ替えることができます。 ケースを日付に基づいて表示したいので、検索機能と並べ替え機能を削除しましょう。 これらのメソッドを組み合わせることもできますが。このアプリでは日付に基づくアプローチに焦点を当てましょう。 下図に追加した項目を示します。

* ユーザーに手順を知らせるテキスト ラベル ("Show cases after:")。**[Insert]\(挿入)** > **[Text]\(テキスト)** > **[Label]\(ラベル)**。**Fill** 式を **White** に変更します。
* 日付の選択。**[Insert]\(挿入)** > **[Controls]\ (コントロール)** > **[Date picker]\(日付の選択)**。
* ブラウズ ギャラリーの **Items** プロパティを日付の選択に接続する数式: `Filter(Case, DatePicker1.SelectedDate < LastModifiedDateTime)`。

日付が年 10 月 20日に設定され、結果として、この日付以降に作成されたケースがアプリに表示されます。 既定では、エンティティのすべてのケースで最終更新日が同じになることに注意してください。 フィルター処理の動作を確認するために、何回か更新してください。 エンティティ データの操作については、コースで後ほど説明します。

![日付の選択を使用するように更新されたアプリ](./media/learning-case-app-customize/date-picker.png)

## <a name="show-total-number-of-cases"></a>ケースの合計数を表示する
ここでは、多くのことを説明していますが、カスタマイズについてはほぼ説明し終わりました。 最後にこのトピックでは、2 つの数値を表示するラベルを追加します。ケースの合計数と、先ほどの日付に基づくフィルターに一致するケース数です。

![合計とフィルター選択されたケース数を表示する](./media/learning-case-app-customize/number-cases.png)

2 つのラベルを追加する方法はビデオで詳しく説明していますが、各ラベルで設定するプロパティの基本事項を次に示します。

* **Align** = `Center`
* **Width** = `Parent.Width/2`
* 左のボックスの **Text** = `"Total cases: " & CountRows(Case)`。 これには、エンティティ内のすべてのケースが含まれます。 
* 右のボックスの **Text** = `Filtered cases: " & CountRows(BrowseGallery1.AllItems)`。 これには、日付に基づくフィルターに一致するケースのみが含まれます。

アプリのカスタマイズは以上です。次のトピックでは、データ ソースとフローを追加して、完成したアプリをお見せします。

