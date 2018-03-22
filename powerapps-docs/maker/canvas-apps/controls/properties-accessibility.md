---
title: アクセシビリティのプロパティ | Microsoft Docs
description: TabIndex、Tooltip などのプロパティに関する参照情報
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
ms.date: 01/26/2017
ms.author: fikaradz
ms.openlocfilehash: d35b4bc7a6e479ce47ad0a0b841a6ed9ccfd1a52
ms.sourcegitcommit: 59785e9e82da8f5bd459dcb5da3d5c18064b0899
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/22/2018
---
# <a name="accessibility-properties-in-powerapps"></a>PowerApps のアクセシビリティのプロパティ
障碍のあるユーザーに適したコントロールを備えた、別の方法での操作を提供するためのプロパティを構成します。

### <a name="properties"></a>プロパティ
**AccessiblityLabel** - スクリーン リーダーによって読み取られるコントロールの説明です。   画像、アイコン、および図形コントロールの値を空にすると、スクリーン リーダーにはコントロールが表示されなくなり、装飾として扱われます。

* **[オーディオ](control-audio-video.md)**、**[ボタン](control-button.md)**、**[カメラ](control-camera.md)****[チェック ボックス](control-check-box.md)**、**[ドロップ ダウン](control-drop-down.md)**、**[HTML テキスト](control-html-text.md)**、**[イメージ](control-image.md)**、**[ラベル](control-text-box.md)**、**[リスト ボックス](control-list-box.md)**、**[マイク](control-microphone.md)**、**[PDF ビューアー](control-pdf-viewer.md)**、**[ペン入力](control-pen-input.md)**、**[ラジオ](control-radio.md)**、**[評価](control-rating.md)**、**[スライダー](control-slider.md)**、**[テキスト入力](control-text-input.md)**、**[タイマー](control-timer.md)**、**[トグル](control-toggle.md)**、および**[ビデオ](control-audio-video.md)**の各コントロールに適用されます。

**TabIndex** – 実行時のコントロールのタブの順序をカスタマイズできます。

既定値 0 は、コントロールの XY 座標に基づいて、既定のタブの順序を指定します。  0 より大きな値を設定すると、コントロールのタブの順序が、既定値が設定されているすべてのコントロールの前に移動されます。  TabIndex 値 2 が設定されているコントロールは、TabIndex 値 3 以上が設定されているコントロールに優先します。

フォームやギャラリーなどのコントロールのコンテナーは、コンテナー外のコントロールに進む前に、コンテナーのすべての要素を常にタブ処理することに注意してください。  コンテナーのタブの順序は、子コントロールの TabIndex の最小値です。

TabIndex を -1 に設定すると、コントロールへのタブのアクセスが無効になります。画像、アイコン、および図形の場合は、非インタラクティブ要素となります。

* **[ボタン](control-button.md)**、**[日付の選択](control-date-picker.md)**、**[ドロップダウン](control-drop-down.md)**、**[イメージ](control-image.md)**、**[インポート](control-export-import.md)**、**[リスト ボックス](control-list-box.md)**、**[ラジオ](control-radio.md)**、**[評価](control-rating.md)**、**[スライダー](control-slider.md)**、**[テキスト入力](control-text-input.md)**、および**[トグル](control-toggle.md)**の各コントロールに適用されます。
