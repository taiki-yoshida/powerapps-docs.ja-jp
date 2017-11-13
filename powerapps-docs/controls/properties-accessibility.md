---
title: "アクセシビリティのプロパティ | Microsoft Docs"
description: "TabIndex、Tooltip などのプロパティに関する参照情報"
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
ms.date: 01/26/2017
ms.author: anneta
ms.openlocfilehash: d8cc9d6c8586856dcaa27f67d3ea1fdc17fa0433
ms.sourcegitcommit: 43be6a4e08849d522aabb6f767a81c092419babc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2017
---
# <a name="accessibility-properties-in-powerapps"></a>PowerApps のアクセシビリティのプロパティ
## <a name="overview"></a>概要
視覚的に障碍のあるユーザーに適したコントロールの別の方法での操作を支援するためのプロパティを構成します。

## <a name="properties"></a>プロパティ
**Tooltip** – ポインターをコントロールに合わせたときに表示される説明テキストです。  テキストは、スクリーン リーダーを補助する Aria ラベルで使用されます。

* **[オーディオ](control-audio-video.md)**、**[ボタン](control-button.md)**、**[カメラ](control-camera.md)****[チェック ボックス](control-check-box.md)**、**[ドロップ ダウン](control-drop-down.md)**、**[HTML テキスト](control-html-text.md)**、**[イメージ](control-image.md)**、**[ラベル](control-text-box.md)**、**[リスト ボックス](control-list-box.md)**、**[マイク](control-microphone.md)**、**[PDF ビューアー](control-pdf-viewer.md)**、**[ペン入力](control-pen-input.md)**、**[ラジオ](control-radio.md)**、**[評価](control-rating.md)**、**[スライダー](control-slider.md)**、**[テキスト入力](control-text-input.md)**、**[タイマー](control-timer.md)**、**[トグル](control-toggle.md)**、および**[ビデオ](control-audio-video.md)**の各コントロールに適用されます。

**TabIndex** – 実行時のコントロールのタブの順序をカスタマイズできます。

既定値 0 は、コントロールの XY 座標に基づいて、既定のタブの順序を指定します。  0 より大きな値を設定すると、コントロールのタブの順序が、既定値が設定されているすべてのコントロールの前に移動されます。  TabIndex 値 2 が設定されているコントロールは、TabIndex 値 3 以上が設定されているコントロールに優先します。

フォームやギャラリーなどのコントロールのコンテナーは、コンテナー外のコントロールに進む前に、コンテナーのすべての要素を常にタブ処理することに注意してください。  コンテナーのタブの順序は、子コントロールの TabIndex の最小値です。

TabIndex を - 1 に設定すると、コントロールへのタブのアクセスが無効になります。イメージ、アイコン、および図形の場合は、スクリーン リーダーにも表示されません。

* **[ボタン](control-button.md)**、**[日付の選択](control-date-picker.md)**、**[ドロップダウン](control-drop-down.md)**、**[イメージ](control-image.md)**、**[インポート](control-export-import.md)**、**[リスト ボックス](control-list-box.md)**、**[ラジオ](control-radio.md)**、**[評価](control-rating.md)**、**[スライダー](control-slider.md)**、**[テキスト入力](control-text-input.md)**、および**[トグル](control-toggle.md)**の各コントロールに適用されます。

