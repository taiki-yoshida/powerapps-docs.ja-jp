---
title: "シェイプ コントロールとアイコン コントロール: リファレンス | Microsoft Docs"
description: "各種プロパティとサンプルを含むシェイプ コントロールとアイコン コントロールに関する情報"
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
ms.openlocfilehash: 7a71695460453816dd5c63dad8477cb7ccc703d7
ms.sourcegitcommit: 43be6a4e08849d522aabb6f767a81c092419babc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2017
---
# <a name="shape-controls-and-icon-controls-in-powerapps"></a>PowerApps のシェイプ コントロールとアイコン コントロール
見た目と動作のプロパティが構成できるグラフィックスです。

## <a name="description"></a>説明
これらのコントロールには、矢印、幾何学的図形、アクション アイコン、記号などがあり、塗りつぶし、サイズ、位置などのプロパティを構成できます。 また、**[OnSelect](properties-core.md)** プロパティを構成すると、ユーザーがコントロールをクリックまたはタップした場合にアプリが反応するようにできます。

## <a name="key-properties"></a>主要なプロパティ
**[Fill](properties-color-border.md)** – コントロールの背景色です。

**[OnSelect](properties-core.md)** – ユーザーがコントロールをタップまたはクリックした場合のアプリの反応を指定します。

## <a name="additional-properties"></a>その他のプロパティ
**[DisplayMode](properties-core.md)** – コントロールで、ユーザー入力を許可するか (**Edit**)、データの表示のみを許可するか (**View**)、許可しないか (**Disabled**) を設定します。

**[Height](properties-size-location.md)** – コントロールの上端と下端の距離です。

**[HoverFill](properties-color-border.md)** – コントロールにユーザーがマウス ポインターを重ねているときのコントロールの背景色です。

**[PressedBorderColor](properties-color-border.md)** – コントロールをユーザーがタップまたはクリックしたときのコントロールの境界線の色です。

**[FocusedBorderThickness](properties-color-border.md)** – キーボードでフォーカスした場合のコントロールの境界線の太さです。

**[Visible](properties-core.md)** – コントロールを表示するか非表示にするかを指定します。

**[Width](properties-size-location.md)** – コントロールの左端と右端の間の距離です。

**[X](properties-size-location.md)** – コントロールの左端とその親コンテナー (親コンテナーがない場合は画面) の左端間の距離です。

**[Y](properties-size-location.md)** – コントロールの上端とその親コンテナー (親コンテナーがない場合は画面) の上端間の距離です。

## <a name="related-functions"></a>関連する関数
[**Navigate**( *ScreenName*, *ScreenTransition* )](../functions/function-navigate.md)

## <a name="example"></a>例
1. 既定の**[スクリーン](control-screen.md)** コントロールに **Target** という名前を付け、**[ラベル](control-text-box.md)** コントロールを追加して **Target** を表示するように **[Text](properties-core.md)** プロパティを設定します。
   
    [コントロールの追加および構成方法](../add-configure-controls.md)については関連記事を参照してください。
2. **[スクリーン](control-screen.md)** コントロールを追加し、**Source** という名前を付けます。
3. **Source** に **シェイプ** コントロールを追加し、**[OnSelect](properties-core.md)** プロパティに次の式を設定します。
   <br>**Navigate(Target, ScreenTransition.Fade)**
4. F5 キーを押してから、**シェイプ** コントロールをクリックまたはタップします。
   
    **[Target]\(ターゲット)** 画面が表示されます。
5. (省略可能) Esc キーを押して既定のワークスペースに戻り、**Target** に**シェイプ** コントロールを追加して、**シェイプ** コントロールの **[OnSelect](properties-core.md)** プロパティに次の式を設定します。
   <br>**Navigate(Source, ScreenTransition.Fade)**

