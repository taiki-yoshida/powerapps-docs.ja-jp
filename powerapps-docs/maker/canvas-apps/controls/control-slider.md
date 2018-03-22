---
title: "スライダー コントロール: リファレンス | Microsoft Docs"
description: "各種プロパティとサンプルを含むスライダー コントロールに関する情報"
services: 
suite: powerapps
documentationcenter: na
author: fikaradz
manager: anneta
editor: 
tags: 
ms.service: powerapps
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/25/2016
ms.author: fikaradz
ms.openlocfilehash: dc10ac44c1c14f182c39176a6b0216f3ede3816d
ms.sourcegitcommit: 33099e6197c0139679cd08c42e9e2a5717904c92
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/12/2018
---
# <a name="slider-control-in-powerapps"></a>PowerApps のスライダー コントロール
ハンドルをドラッグして値を指定できるコントロールです。

## <a name="description"></a>説明
ユーザーは、スライダーのハンドルを左右または上下 (あなたが選択した方向) にドラッグして、指定された最小値と最大値の間の値を指定できます。

## <a name="key-properties"></a>主要なプロパティ
**[Default](properties-core.md)** – ユーザーが変更する前のコントロールの初期値です。

**Max** – ユーザーがスライダーまたは評価を設定できる最大値です。

**Min** – ユーザーがスライダーを設定できる最小値です。

**[Value](properties-core.md)** – 入力コントロールの値です。

## <a name="additional-properties"></a>その他のプロパティ
**[BorderColor](properties-color-border.md)** – コントロールの境界線の色です。

**[BorderStyle](properties-color-border.md)** – コントロールの境界線を **Solid** (実線)、**Dashed** (破線)、**Dotted** (点線)、**None** (なし) のいずれに指定します。

**[BorderThickness](properties-color-border.md)** – コントロールの境界線の太さです。

**[FocusedBorderThickness](properties-color-border.md)** – キーボードでフォーカスした場合のコントロールの境界線の太さです。

**[DisplayMode](properties-core.md)** – コントロールで、ユーザー入力を許可するか (**Edit**)、データの表示のみを許可するか (**View**)、許可しないか (**Disabled**) を設定します。

**[DisabledBorderColor](properties-color-border.md)** – コントロールの **[DisplayMode](properties-core.md)** プロパティが **Disabled** に設定されている場合のコントロールの境界線の色です。

**HandleActiveFill** – ユーザーが値を変更しているときのスライダーのハンドルの色です。

**HandleFill** – トグルまたはスライダー コントロールのハンドル (位置が変わる要素) の色です。

**HandleHoverFill** – スライダーのハンドルにユーザーがマウス ポインターを重ねているときのハンドルの色です。

**[Height](properties-size-location.md)** – コントロールの上端と下端の距離です。

**[HoverBorderColor](properties-color-border.md)** – コントロール上にユーザーがマウス ポインターを重ねているときのコントロールの境界線の色です。

**Layout** – ユーザーがギャラリーをスクロールしたりスライダーを調整したりする方向です。上下 (**Vertical**) または左右 (**Horizontal**) から選択します。

**[OnChange](properties-core.md)** – ユーザーが (スライダーを調整するなどして) コントロールの値を変更した場合のアプリの反応を指定します。

**[OnSelect](properties-core.md)** – ユーザーがコントロールをタップまたはクリックした場合のアプリの反応を指定します。

**[PressedBorderColor](properties-color-border.md)** – コントロールをユーザーがタップまたはクリックしたときのコントロールの境界線の色です。

**RailFill** – 値が **false** の場合の、トグル コントロール内の四角形の背景色、またはスライダー コントロールのハンドルの右側の線の色です。

**RailHoverFill** – 値が **false** の場合に、トグル コントロールまたはスライダーをポイントしたときの、トグル コントロール内の四角形の背景色、またはスライダー コントロールのハンドルの右側の線の色です。

**ReadOnly** – ユーザーがスライダーまたは評価コントロールの値を変更できるかどうかを指定します。

**[Reset](properties-core.md)** – コントロールを既定値に戻すかどうかを指定します。

**ShowValue** – ユーザーがスライダーまたは評価の値を変更するか、ポインタをコントロールに合わせたときにその値を表示するかどうかを指定します。

**[TabIndex](properties-accessibility.md)** – ゼロ以外の値に設定すると、実行時のコントロールのタブの順序をカスタマイズできます。

**[Tooltip](properties-core.md)** – ポインターをコントロールに合わせたときに表示される説明テキストです。

**ValueFill** – 値が **true** の場合の、トグル コントロール内の四角形の背景色、またはスライダー コントロールのハンドルの左側の線の色です。

**ValueHoverFill** – 値が **true** の場合に、トグル コントロールまたはスライダーをポイントしたときの、トグル コントロール内の四角形の背景色、またはスライダー コントロールのハンドルの左側の線の色です。

**[Visible](properties-core.md)** – コントロールを表示するか非表示にするかを指定します。

**[Width](properties-size-location.md)** – コントロールの左端と右端の間の距離です。

**[X](properties-size-location.md)** – コントロールの左端とその親コンテナー (親コンテナーがない場合は画面) の左端間の距離です。

**[Y](properties-size-location.md)** – コントロールの上端とその親コンテナー (親コンテナーがない場合は画面) の上端間の距離です。

## <a name="related-functions"></a>関連する関数
[**Sum**( *Value1*, *Value2* )](../functions/function-aggregates.md)

## <a name="example"></a>例
1. ボタンを追加し、**[OnSelect](properties-core.md)** プロパティを次の数式に設定します。
   <br>**ClearCollect(CityPopulations, {City:"London", Country:"United Kingdom", Population:8615000}, {City:"Berlin", Country:"Germany", Population:3562000}, {City:"Madrid", Country:"Spain", Population:3165000}, {City:"Rome", Country:"Italy", Population:2874000}, {City:"Paris", Country:"France", Population:2273000}, {City:"Hamburg", Country:"Germany", Population:1760000}, {City:"Barcelona", Country:"Spain", Population:1602000}, {City:"Munich", Country:"Germany", Population:1494000}, {City:"Milan", Country:"Italy", Population:1344000})**
   
    [コントロールの追加、命名、構成についてはこちらをご覧ください](../add-configure-controls.md)。
   
    **[ClearCollect](../functions/function-clear-collect-clearcollect.md)** 関数または[その他の関数](../formula-reference.md)については各関連記事を参照してください。
2. F5 キーを押して、ボタンを選択し、Esc キーを押します。
3. スライダーを追加して、ボタンの下に移動し、スライダーに「**MinPopulation**」と名前を付けます。
4. スライダーの **Max** プロパティを「**5000000**」、**Min** プロパティを「**1000000**」に設定します。
5. テキスト ギャラリーを垂直方向 (縦向き) で追加して、スライダーの下に移動し、ギャラリーの **[Items](properties-core.md)** プロパティを次の数式に設定します。<br>
   **Filter(CityPopulations, Population > MinPopulation)**
6. ギャラリーの最初の項目で、上のラベルの **[Text](properties-core.md)** プロパティを「**ThisItem.City**」に、下のラベルの **[Text](properties-core.md)** プロパティを次の数式に設定します。<br> **Text(ThisItem.Population, "##,###")**
7. F5 キーを押して、**MinPopulation** を調整し、指定した値よりも人口が多い都市のみを表示します。
8. 既定のワークスペースに戻るには、Esc キーを押します。

