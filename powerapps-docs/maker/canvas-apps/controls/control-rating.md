---
title: '評価コントロール: リファレンス | Microsoft Docs'
description: 各種プロパティとサンプルを含む評価コントロールに関する情報
services: ''
suite: powerapps
documentationcenter: na
author: fikaradz
manager: anneta
editor: ''
tags: ''
ms.service: powerapps
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/25/2016
ms.author: fikaradz
ms.openlocfilehash: 4dd23b8c94ee4760e40b4513e7a88667f85c3a4b
ms.sourcegitcommit: 59785e9e82da8f5bd459dcb5da3d5c18064b0899
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/22/2018
---
# <a name="rating-control-in-powerapps"></a>PowerApps の評価コントロール
ユーザーが 1 から指定された最大数までの値を示すために使用できるコントロールです。

## <a name="description"></a>説明
このコントロールでは、たとえば、ユーザーがあるものをどれだけ気に入ったかを特定数の星を選択して示すことができます。

## <a name="key-properties"></a>主要なプロパティ
**[Default](properties-core.md)** – ユーザーが変更する前のコントロールの初期値です。

**Max** – ユーザーがスライダーまたは評価を設定できる最大値です。

## <a name="additional-properties"></a>その他のプロパティ
**[BorderColor](properties-color-border.md)** – コントロールの境界線の色です。

**[BorderStyle](properties-color-border.md)** – コントロールの境界線を **Solid** (実線)、**Dashed** (破線)、**Dotted** (点線)、**None** (なし) のいずれに指定します。

**[BorderThickness](properties-color-border.md)** – コントロールの境界線の太さです。

**[FocusedBorderThickness](properties-color-border.md)** – キーボードでフォーカスした場合のコントロールの境界線の太さです。

**[DisplayMode](properties-core.md)** – コントロールで、ユーザー入力を許可するか (**Edit**)、データの表示のみを許可するか (**View**)、許可しないか (**Disabled**) を設定します。

**[Fill](properties-color-border.md)** – コントロールの背景色です。

**[Height](properties-size-location.md)** – コントロールの上端と下端の距離です。

**[OnChange](properties-core.md)** – ユーザーが (スライダーを調整するなどして) コントロールの値を変更した場合のアプリの反応を指定します。

**[OnSelect](properties-core.md)** – ユーザーがコントロールをタップまたはクリックした場合のアプリの反応を指定します。

**RatingFill** – 評価コントロールの星の色です。

**ReadOnly** – ユーザーがスライダーまたは評価コントロールの値を変更できるかどうかを指定します。

**[Reset](properties-core.md)** – コントロールを既定値に戻すかどうかを指定します。

**ShowValue** – ユーザーがスライダーまたは評価の値を変更するか、ポインタをコントロールに合わせたときにその値を表示するかどうかを指定します。

**[TabIndex](properties-accessibility.md)** – ゼロ以外の値に設定すると、実行時のコントロールのタブの順序をカスタマイズできます。

**[Tooltip](properties-core.md)** – ポインターをコントロールに合わせたときに表示される説明テキストです。

**[Visible](properties-core.md)** – コントロールを表示するか非表示にするかを指定します。

**[Width](properties-size-location.md)** – コントロールの左端と右端の間の距離です。

**[X](properties-size-location.md)** – コントロールの左端とその親コンテナー (親コンテナーがない場合は画面) の左端間の距離です。

**[Y](properties-size-location.md)** – コントロールの上端とその親コンテナー (親コンテナーがない場合は画面) の上端間の距離です。

## <a name="related-functions"></a>関連する関数
[**Average**( *Value1*, *Value2,* ... )](../functions/function-aggregates.md)

## <a name="example"></a>例
1. **評価**コントロールを追加して **Quantitative** という名前を付けます。
   
    [コントロールの追加、命名、構成についてはこちらをご覧ください](../add-configure-controls.md)。
2. **[テキスト入力](control-text-input.md)**コントロールを追加して **Qualitative** という名前を付け、**評価**コントロールの下に移動します。
3. **[テキスト入力](control-text-input.md)**コントロールの **[Default](properties-core.md)** プロパティを **""** に設定し、その **HintText** を次の数式に設定します。
   <br>**If(Quantitative.Value > 3, "何が特に気に入りましたか?", "どのようにした方がいいでしょうか?")**
   
    **[If](../functions/function-if.md)** 関数または[その他の関数](../formula-reference.md)については各関連記事を参照してください。
4. F5 キーを押して、**評価**コントロールの 4 つか 5 つの星をクリックまたはタップします。
   
    **[テキスト入力](control-text-input.md)**コントロールのヒント テキストが、高い評価を反映して変更されます。
5. **Quantitative** の 4 つより少ない星をクリックまたはタップします。
   
    **[テキスト入力](control-text-input.md)**コントロールのヒント テキストが、低い評価を反映して変更されます。
6. 既定のワークスペースに戻るには、Esc キーを押します。

