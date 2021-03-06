---
title: 演算子 | Microsoft Docs
description: PowerApps の演算子に関する構文と例を含む参照情報
services: ''
suite: powerapps
documentationcenter: na
author: gregli-msft
manager: anneta
editor: ''
tags: ''
ms.service: powerapps
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 07/24/2017
ms.author: gregli
ms.openlocfilehash: 3250251e02170d2dd7bab441bc3c94705216ec00
ms.sourcegitcommit: 59785e9e82da8f5bd459dcb5da3d5c18064b0899
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/22/2018
---
# <a name="operators-and-data-types-in-powerapps"></a>PowerApps の演算子とデータ型
これらの演算子の一部は、作成者の言語に依存します。  詳細については、[グローバル アプリ](../global-apps.md)に関する記事を参照してください。

| 記号 | 種類 | 構文 | 説明 |
| --- | --- | --- | --- |
| **.** |プロパティ セレクター |**Slider1.Value<br>Color.Red<br>Acceleration.X** |[テーブル](../working-with-tables.md)、コントロール[、シグナル](signals.md)または列挙からプロパティを抽出します。  旧バージョンとの互換性のために **!** を使用することもできます。 |
| **.**<br>[または **,** ([言語による](../global-apps.md))] |小数点 |**1.23**<br>[または **1,23** (言語による)] |数値の整数部分と小数部分の区切り記号。  この文字は言語に依存します。 |
| **( )** |かっこ |**Filter(T, A &lt; 10)**<br><br>**(1 + 2) * 3** |優先順位を変更し、式の中の副次式をグループ化します。 |
| **+** |算術演算子 |**1 + 2** |加算 |
| **-** |&nbsp; |**2 - 1** |減算および符号 |
| **\*** |&nbsp; |**2 * 3** |乗算 |
| **/** |&nbsp; |**2 / 3** |除算 ( **[Mod](function-mod.md)** 関数も参照してください) |
| **^** |&nbsp; |**2 ^ 3** |累乗。**[Power](function-numericals.md)** 関数に相当します |
| **%** |&nbsp; |**20%** |百分率 (&quot;* 1/100&quot; に相当します) |
| **=** |比較演算子 |**Price = 100** |等しい |
| **&gt;** |&nbsp; |**Price &gt; 100** |超 |
| **&gt;=** |&nbsp; |**Price &gt;= 100** |以上 |
| **&lt;** |&nbsp; |**Price &lt; 100** |未満 |
| **&lt;=** |&nbsp; |**Price &lt;= 100** |以下 |
| **&lt;&gt;** |&nbsp; |**Price &lt;&gt; 100** |等しくない |
| **&amp;** |文字列連結演算子 |**&quot;hello&quot; &amp; &quot; &quot; &amp; &quot;world&quot;** |複数の文字列を続けて表示します |
| **&amp;&amp;** または **And** |論理演算子 |**Price &lt; 100 &amp;&amp; Slider1.Value = 20**<br>または **Price &lt; 100 And Slider1.Value = 20** |論理積。**[And](function-logicals.md)** 関数に相当します |
| **&#124;&#124;** または **Or** |&nbsp; |**Price &lt; 100 &#124;&#124; Slider1.Value = 20** または **Price &lt; 100 Or Slider1.Value = 20** |論理和。**[Or](function-logicals.md)** 関数に相当します |
| **!** または **Not** |&nbsp; |**!(Price &lt; 100)** または **Not (Price &lt; 100)** |論理否定。**[Not](function-logicals.md)** 関数に相当します |
| **exactin** |[メンバーシップ演算子](#in-and-exactin-operators) |**Gallery1.Selected exactin SavedItems** |[コレクション](../working-with-data-sources.md#collections)またはテーブルに属しています |
| **exactin** |&nbsp; |**&quot;Windows&quot; exactin “To display windows in the Windows operating system...”** |部分文字列をテストします (大文字小文字を区別します) |
| **in** |&nbsp; |**Gallery1.Selected in SavedItems** |コレクションまたはテーブルに属しています |
| **in** |&nbsp; |**&quot;The&quot; in &quot;The keyboard and the monitor...&quot;** |部分文字列をテストします (大文字小文字を区別しません) |
| **@** |[曖昧性除去演算子](#disambiguation-operator) |**MyTable[@fieldname]** |フィールドの曖昧性を除去します |
| **@** |&nbsp; |**[@MyVariable]** |グローバルの曖昧性を除去します |
| **,**<br>[または **;** ([言語による](../global-apps.md))] |リストの区切り記号 |**If( X < 10, "Low", "Good" )**<br>**{ X: 12, Y: 32 }**<br>**[ 1, 2, 3 ]**<br>[または **If( X < 10; "Low"; "Good" )<br>{ FirstName: "Jane"; LastName: "Doe" }<br>[ 1; 2; 3 ]** ] |以下の要素を区切ります。 <ul><li>関数呼び出しの引数</li><li>[レコード](../working-with-tables.md#elements-of-a-table)のフィールド</li><li>[値テーブル](../working-with-tables.md#inline-syntax)のレコード</li></ul>.  この文字は言語に依存します。 |
| **;**<br>[または **;;** ([言語による](../global-apps.md))] |数式のチェーン |**Collect(T, A); Navigate(S1, &quot;&quot;)**<br>[または **Collect(T; A);; Navigate(S1; &quot;&quot;)**] |関数の呼び出しの動作プロパティを区切ります。  このチェーン演算子は言語に依存します。 |
| **Parent** |[Parent 演算子](#parent-operator) |**Parent.Fill** |コントロール コンテナーのプロパティにアクセスします |
| **ThisItem** |[ThisItem 演算子](#thisitem-operator) |**ThisItem.FirstName** |ギャラリーまたはフォーム コントロールのフィールドにアクセスします |

## <a name="in-and-exactin-operators"></a>in 演算子と exactin 演算子
**[in](operators.md#in-and-exactin-operators)** 演算子と **[exactin](operators.md#in-and-exactin-operators)** 演算子を使用して、コレクションやインポートされたテーブルなどの[データ ソース](../working-with-data-sources.md)内の文字列を検索できます。 **[in](operators.md#in-and-exactin-operators)** 演算子は、大文字小文字を無視して一致する文字列を識別し、**[exactin](operators.md#in-and-exactin-operators)** 演算子は、大文字小文字が一致する文字列のみを識別します。 次に例を示します。

1. **Inventory** という名前のコレクションを作成するかインポートし、「[Show images and text in a gallery](../show-images-text-gallery-sort-filter.md)」 (イメージとテキストをギャラリーに表示する) の最初の手順に従って、ギャラリーに表示します。
2. ギャラリーの **[Items](../controls/properties-core.md)** プロパティを次の数式に設定します。
   <br>**Filter(Inventory, "E" in ProductName)**
   
    ギャラリーには、指定した文字が名前に含まれていない唯一の製品である Callisto を除くすべての製品が表示されます。
3. ギャラリーの **[Items](../controls/properties-core.md)** プロパティを次の数式に変更します。
   <br>**Filter(Inventory, "E" exactin ProductName)**
   
    ギャラリーには、指定した大文字が名前に含まれている唯一の製品である Europa のみが表示されます。

## <a name="thisitem-operator"></a>ThisItem 演算子
**[ギャラリー](../controls/control-gallery.md)**、**[編集フォーム](../controls/control-form-detail.md)**、または**[表示フォーム](../controls/control-form-detail.md)** コントロールをテーブルまたはコレクションにバインドすることによって、テーブルまたはコレクションのデータを表示することができます。  これらのコントロールは、他のカードまたはコントロールのコンテナーです。  コンテナー内のカードまたはコントロールは、**[ThisItem](operators.md#thisitem-operator)** 演算子を通して、バインドされているデータにアクセスできます。   

**[ThisItem](operators.md#thisitem-operator)** 演算子を使用して、外側のカードまたはコントロール内の[列](../working-with-tables.md#columns)を指定します。 たとえば、「[Show images and text in a gallery](../show-images-text-gallery-sort-filter.md)」 (イメージとテキストをギャラリーに表示する) の製品ギャラリーでは、この演算子は、製品のデザインを表示するイメージ コントロール、製品名を表示する上のラベル、および在庫数を示す下のラベルを指定しています。

入れ子になっているギャラリーでは、**[ThisItem](operators.md#thisitem-operator)** は、最も内側のギャラリー アイテムを参照します。 内側と外側のギャラリーの行フィールドが競合していないことを前提として、修飾されていないフィールド (列) 名を直接使用することもできます。 この方法によって、内側のギャラリーが外側のギャラリーのアイテムを参照するというルールが有効になります。

## <a name="parent-operator"></a>Parent 演算子
一部のコントロールは、その他のコントロールをホストします。 たとえば、**[画面](../controls/control-screen.md)****[ギャラリー](../controls/control-gallery.md)****[カード](../controls/control-card.md)****[編集フォーム](../controls/control-form-detail.md)**および**[表示フォーム](../controls/control-form-detail.md)**コントロールは、すべてがコントロールのコンテナーです。 ホストしているコントロールは、その中に含まれているコントロールの "親" と呼ばれます。

PowerApps のコントロールは、アプリ内のどこからでも、名前で参照することができます。 **Screen1** がアプリの画面名であるとします。 この画面の背景色を取得するには、**Screen1.Fill** を使用できます。

この画面上のコントロールには、別のオプションがあります。 それらは、相対参照である **Parent.Fill** を使用することができます。 **[Parent](operators.md#parent-operator)** 演算子は、コントロールをホストしているコントロールを参照して、ホストしているコントロールのすべてのプロパティを使用できるようにします。 **[Parent](operators.md#parent-operator)** コントロールはコントロールの名前に依存しないため、便利に使用できます。 コンテナー コントロールは、コンテナー内の参照の調整なしで、コピーして貼り付けることができます。 さらに、この演算子は、数式を読み取るときに、コントロールの親子関係を理解しやすくします。

## <a name="disambiguation-operator"></a>曖昧性除去演算子
一部の関数では、各レコードの処理中に、テーブルのフィールドにアクセスするための[レコード スコープ](../working-with-tables.md#record-scope)を作成します (**Filter**、**AddColumns**、**Sum** など)。  レコード スコープによって追加されたフィールド名は、アプリの別の場所にある同じ名前に優先します。  これが発生した場合でも、**@** 曖昧性除去演算子を使用して、レコード スコープの外部の値にアクセスできます。

* 入れ子になったレコード スコープの値にアクセスするには、**@** 演算子と操作対象のテーブルの名前を ***テーブル*[@*フィールド名*]** のパターンで使用します。  
* データ ソース、コレクション、コンテキスト変数などのグローバル値にアクセスするには、**[@*オブジェクト名*]** のパターンを使用します (テーブルは指定しません)。

詳細と例については、「[record scopes](../working-with-tables.md#record-scope)」 (レコード スコープ)を参照してください。

