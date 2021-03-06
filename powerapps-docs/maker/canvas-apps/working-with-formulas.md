---
title: 数式を利用する | Microsoft Docs
description: 数式を利用してアプリをカスタマイズします。
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
ms.date: 04/26/2016
ms.author: gregli
ms.openlocfilehash: 076b9a67d700cc318491471182fe273b2edaaff9
ms.sourcegitcommit: 59785e9e82da8f5bd459dcb5da3d5c18064b0899
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/22/2018
---
# <a name="get-started-with-formulas"></a>数式の使用を開始
(Excel で行われるように) 値を計算してその他のタスクを実行するだけでなく、(アプリが必要とするように) ユーザー入力に応答する数式を利用して、アプリを構成します。

* Excel では、たとえばセルに入力を行ってテーブルとグラフを作成する数式を構築します。
* PowerApps では、セルではなくコントロールを構成し、同様の数式を構築します。 さらに、スプレッドシートではなく特定のアプリに適用される数式を構築します。

たとえば、ボタンの選択、スライダーの調整、またはその他の入力がユーザーによって行われた場合にアプリがどのように応答するかを決定する数式を構築します。 これらの数式により、異なる画面を表示したり、アプリの外部にあるデータ ソースを更新したり、既存のテーブルに存在するデータのサブセットが含まれたテーブルを作成したりできます。

数式は、さまざまなシナリオで利用できます。 たとえば、**Location.Latitude** と **Location.Longitude** が使用される数式、デバイスの GPS、マップ コントロールを使って、現在の場所を表示できます。 移動すると、マップによって場所が自動的に追跡されます。

このトピックでは、数式の操作の概要のみを示します。 詳しい情報のほか、使用できる関数、演算子、その他の構成要素の完全な一覧については、[数式のリファレンス](formula-reference.md)を参照してください。

## <a name="prerequisites"></a>前提条件

* PowerApps に[サインアップ](../signup-for-powerapps.md)し、[インストール](http://aka.ms/powerappsinstall)して開きます。その後、サインアップに使用したのと同じ資格情報を入力してサインインします。
* PowerApps で[コントロールを構成する](add-configure-controls.md)方法について確認します。

## <a name="show-a-simple-value"></a>単純な値の表示
Excel では、「**42**」という数字や「**Hello World**」というフレーズなど、特定のデータをセルに打ち込んで入力できます。 このセルには、常に入力したとおりにデータが表示されます。 PowerApps では、同じように変更されないデータを指定できます。これを行うには、ラベルの **[Text](controls/properties-core.md)** プロパティに目的の一連の文字を二重引用符で囲んで正確に設定します。

1. (画面の左端にある) **[File (ファイル)]** メニューの **[New (新規)]** を選択します。
2. **[Create an app (アプリの作成)]** で、**[Blank app (空のアプリ)]** タイルの **[Phone layout (Phone レイアウト)]** を選択します。
   
    数式バーは画面の最上部にあります。
   
    ![数式バー](./media/working-with-formulas/formula-bar.png)
   
    このバーには、2 つの部分があります。
   
   * "*プロパティの一覧*": 各コントロールと画面には[プロパティ](reference-properties.md)があります。  この一覧を使って特定のプロパティを選択します。  
   * "*数式*": 上記のプロパティの計算に使用される数式。[値、演算子、関数](formula-reference.md)で構成されます。
     
     数式バーで、選択したコントロールのプロパティを表示して編集できます。また、コントロールが選択されていない場合は、画面のプロパティを表示して編集できます。  選択されたコントロールの名前は、**[Content (コンテンツ)]** タブで確認できます。
     
     ![現在選択されているコントロールを表示するコンテンツ バー](./media/working-with-formulas/content-tab-selection.png)
     
     **[Content (コンテンツ)]** タブで名前をクリックして、選択されているコントロールの名前を変更できます。
3. 画面に**[ラベル](controls/control-text-box.md)** コントロールを追加します。
   
    ![テキスト ボックス コントロールの追加](./media/working-with-formulas/add-a-label.png)
   
    ラベルを追加すると、プロパティの一覧に **[Text](controls/properties-core.md)** プロパティが自動的に表示されます。このプロパティで、コントロールに表示される内容が決まります。 既定では、このプロパティの値は **"Text"** になっています。  
4. **[Text](controls/properties-core.md)** プロパティの値を **"Hello World"** に設定します。このとき、この文字列を二重引用符で囲んで数式バーに入力します。
   
    ![ラベル "Hello World" の使用](./media/working-with-formulas/label-hello-world.png)
   
    入力が済むと、新しいこの値がラベルに反映されます。  入力中、黄色の感嘆符アイコンが画面に表示される場合があります。 これらのアイコンはエラーを示します。しかし、有効な値の入力を完了すると、表示されなくなります。 たとえば、両側に二重引用符のない文字列は無効です。
   
    Excel では、**42** などの数値を表示するには、その数値をセルに入力したり、その数値が解となる数式 (**=SUM(30,12)** など) を入力したりします。 PowerApps では、ラベルなどのコントロールの **Text** プロパティに **42** または **Sum(30,12)** を設定することで、同じ結果を得ることができます。 ワークシートまたはアプリのその他の変更に関係なく、セルとラベルにはいつもこの数値が表示されます。
   
    > [!NOTE]
> PowerApps では、Excel のように数式の前に等号またはプラス記号を使用することはありません。 数式バーでは、そこに入力したものはすべて既定で数式として処理されます。 さらに、先ほどテキストの文字列を指定したときのように、二重引用符 (") で数式を囲むことはしません。
5. ラベルの **[Text](controls/properties-core.md)** プロパティで、**"Hello World"** を **Sum(1,2,3)** に置き換えます。
   
    ![「Sum(1,2,3」のように部分関数を終わりかっこなしで入力すると、エラーが発生します。](./media/working-with-formulas/label-sum-partial.png)
   
    入力中、数式バーにこの関数の説明と必要な引数が表示されます。  **"Hello World"** の末尾の二重引用符と同様に、この数式の末尾のかっこを入力するまで、画面にはエラーを示す黄色の感嘆符が表示されます。
   
    ![完全な数式 Sum(1,2,3) の使用](./media/working-with-formulas/label-sum.png)

## <a name="change-a-value-based-on-input"></a>入力に基づいた値の変更
Excel では、「**=SUM(A1:A2)**」とセルに入力すると、セル A1 と A2 に含まれている値の合計が表示されます。 これらの値の一方または両方が変更されると、数式が含まれているセルには、更新された結果が自動的に表示されます。

![2 つの数値の合計を再計算する Excel の図](./media/working-with-formulas/excel-recalc.png)

PowerApps では、コントロールを追加してそのプロパティを設定することで、同様の結果を得ることができます。 次の例には、前の手順で使用したラベルのほか、**TextInput1** と **TextInput2** という名前の 2 つの**[テキスト入力](controls/control-text-input.md)**コントロールが示されています。

![2 つの数値の合計を再計算する PowerApps の図](./media/working-with-formulas/recalc1.png)

テキスト入力コントロールにどのような数値を入力しても、ラベルにはいつもその数値の合計が表示されます。これは、**[Text](controls/properties-core.md)** プロパティに次の数式が設定されているためです。
<br>**TextInput1 + TextInput2**

![2 つの数値の合計を再計算する PowerApps の図](./media/working-with-formulas/recalc2.png)

Excel では、たとえば負の値を赤色で表示するなど、条件付き書式を使用できます。 PowerApps では、**[If](functions/function-if.md)** 関数が含まれた数式を使用して、Excel と同様の動作を実現します。

1. ラベルの **[Color](controls/properties-color-border.md)** プロパティに次の数式を設定します。<br>**If( Value(TextBox1.Text) < 0, Red, Black )**
   
    > [!NOTE]
> 数式では、コントロールのプロパティを指定する際に、コントロールの名前、ピリオド、プロパティの名前を順番に入力します。 たとえば、**TextBox1** の **[Text](controls/properties-core.md)** プロパティは、「**TextBox1.Text**」と入力して指定します。
   
    ![値に基づいてラベルの色の変更を再計算する PowerApps の図](./media/working-with-formulas/recalc-color1.png)
2. **TextInput1** と **TextInput2** に、合計すると負の数値になる 2 つの数値を指定します。
   
    ![値に基づいてラベルの色の変更を再計算する PowerApps の図](./media/working-with-formulas/recalc-color2.png)
   
    ラベルの値が赤色で表示されます。

## <a name="change-a-color-based-on-user-input"></a>ユーザー入力に基づいた色の変更
ユーザーがアプリの外観または動作を変更できるように、数式を使用してアプリを構成できます。 たとえば、フィルターを作成してユーザーが指定したテキストの文字列が含まれたデータのみを表示したり、データ セット内のある特定の列に基づいて一連のデータをユーザーが並べ替えられるようにしたりできます。 この手順では、1 つ以上のスライダーを調整することで、ユーザーが画面の色を変更できるようにします。

1. 前の手順のコントロールを削除します。または、先ほど行ったように空のアプリを作成します。その後、3 つのスライダー コントロールを追加します。
   
    ![スライダー コントロールの挿入](./media/working-with-formulas/insert-slider.png)
2. 重ならないようにスライダーを配置し、3 つのラベルを追加して、**Red**、**Green**、**Blue** と表示されるように構成します。
   
    ![スライダーの配置と各色コンポーネントのラベルの追加](./media/working-with-formulas/three-sliders.png)
3. 各スライダーの **Max** プロパティを 255 に設定します。この値は、**[RGBA](functions/function-colors.md)** 関数の色コンポーネントの最大値です。
   
    **Max** プロパティを **[Content (コンテンツ)]** タブまたはプロパティの一覧で選択することで指定できます。
   
    ![各スライダーの最大値の変更](./media/working-with-formulas/three-sliders-max.png)
4. コントロールから離れた場所をクリックして画面を選択し、画面の **[Fill](controls/properties-color-border.md)** プロパティに次の数式を設定します。<br>**RGBA( Slider1.Value, Slider2.Value, Slider3.Value, 1 )**
   
    既に説明したとおり、コントロール プロパティへのアクセスには **.** 。  **Slider1.Value** はスライダーの **[Value](controls/properties-core.md)** プロパティを参照し、ユーザーが **Min** と **Max** の間の値で設定したスライダーの位置が反映されます。 この数式を入力すると、数式に含まれている各コントロールには画面と数式バーで同じ色が付きます。
   
    ![画面の背景塗りつぶし色に関する数式の変更 (未完了)](./media/working-with-formulas/three-sliders-partial-rgba.png)
   
    閉じかっこを入力すると、各スライダーの既定の値 (**50**) に基づいて、画面の背景が濃い灰色に変わります。 数式の入力が完了した瞬間に計算が行われ、背景塗りつぶし色の値として使用されます。 既定のワークスペースでアプリを対話的に操作でき、プレビューを開く必要がありません。
   
    ![各スライダーの最大値の変更](./media/working-with-formulas/three-sliders-complete-rgba.png)
5. スライダーを調整し、変更が背景色に与える影響を確認します。
   
    各スライダーを変更すると、**[RGBA](functions/function-colors.md)** 関数が含まれている数式が再計算され、画面の表示がすぐに変更されます。
   
    ![画面の背景塗りつぶし色に関する数式の変更 (完了)](./media/working-with-formulas/three-sliders-example-colors.png)

## <a name="manage-app-behavior"></a>アプリの動作の管理
数式は、計算の実行と外観の変更だけでなく、アクションの実行にも利用できます。 たとえば、ボタンの **[OnSelect](controls/properties-core.md)** プロパティに、**[Navigate](functions/function-navigate.md)** 関数が含まれた数式を設定できます。 ユーザーがこのボタンを選択すると、数式で指定されている画面が表示されます。

**[Navigate](functions/function-navigate.md)** 関数や **[Collect](functions/function-clear-collect-clearcollect.md)** 関数など、いくつかの関数は動作の数式でのみ使用できます。  このコンテキスト内のみで関数を使用できる場合に、数式参照による呼び出しが行われます。  

セミコロン (;) で関数を分離すると、動作の数式で複数のアクションを実行することができます。 たとえば、コンテキスト変数を更新してデータ ソースにデータをプッシュし、最後に別の画面に移動することができます。

## <a name="view-a-list-of-properties-by-category"></a>カテゴリ別のプロパティの一覧表示
プロパティの一覧では、プロパティがアルファベット順で表示されます。しかし、**[View (表示)]** タブの **[Advanced (詳細)]** オプションを選択すると、(カテゴリ別に整理して) コントロールのプロパティをすべて表示することもできます。

![[Advanced (詳細)] ビュー](./media/working-with-formulas/advanced-open.png)

このビューの中で直接数式を編集できます。  ウィンドウの最上部にあるコントロール セレクタ―では、操作するコントロールをすばやく見つけることができます。  また、プロパティの検索を使用すると、そのコントロールのプロパティをすばやく見つけることができます。

最初に、このビューには最も重要なプロパティが表示されます。  すべてのプロパティを表示するには、ウィンドウの下部にある下向き矢印をクリックします。  各コントロールには、コントロールの動作と外観のあらゆる要素を制御するプロパティの長い一覧があります。 一覧をスクロールしたり、ウィンドウの上部にあるボックスに入力してプロパティを検索したりできます。

## <a name="formula-syntax"></a>数式の構文
数式バーに数式を入力すると、異なる構文要素がそれぞれ別の色で表示され、読みやすさが向上し、長い数式をより簡単に理解できるようになりました。 PowerApps のカラー コードの一覧を示します。

![構文の強調表示](./media/working-with-formulas/syntax-highlighting.png)

