---
title: テキストのプロパティ | Microsoft Docs
description: Text、Tooltip、HintText などのプロパティのリファレンス
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
ms.date: 10/25/2016
ms.author: gregli
ms.openlocfilehash: 6d79f5a93fd89de1c3994f43c285e9d96cb00af6
ms.sourcegitcommit: 59785e9e82da8f5bd459dcb5da3d5c18064b0899
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/22/2018
---
# <a name="text-properties-in-powerapps"></a>PowerApps のテキスト プロパティ
ユーザーのデータ入力時にコントロールのツールヒントにヒントとして表示されるテキストを構成し、その他のテキストに関する特性を指定します。

## <a name="text-appearance"></a>テキストの見た目
**Font** – テキストを表記するフォントのファミリー名です。

* **[画像の追加](control-add-picture.md)**、**[ボタン](control-button.md)**、**[チェック ボックス](control-check-box.md)**、**[縦棒グラフ](control-column-line-chart.md)**、**[日付の選択](control-date-picker.md)**、**[ドロップ ダウン](control-drop-down.md)**、**[エクスポート](control-export-import.md)**、**[HTML テキスト](control-html-text.md)**、**[インポート](control-export-import.md)**、**[ラベル](control-text-box.md)**、**[折れ線グラフ](control-column-line-chart.md)**、**[リスト ボックス](control-list-box.md)**、**[円グラフ](control-pie-chart.md)**、**[ラジオ](control-radio.md)**、**[テキスト入力](control-text-input.md)**、**[タイマー](control-timer.md)**の各コントロールに適用されます。

**FontWeight** – コントロール内のテキストの太さです。**Bold** (太字)、**Semibold** (中太)、**Normal** (標準)、**Lighter** (細字) から指定します。

* **[画像の追加](control-add-picture.md)**、**[ボタン](control-button.md)**、**[チェック ボックス](control-check-box.md)**、**[日付の選択](control-date-picker.md)**、**[ドロップ ダウン](control-drop-down.md)**、**[エクスポート](control-export-import.md)**、**[インポート](control-export-import.md)**、**[ラベル](control-text-box.md)**、**[リスト ボックス](control-list-box.md)**、**[ラジオ](control-radio.md)**、**[テキスト入力](control-text-input.md)**、**[タイマー](control-timer.md)**の各コントロールに適用されます。

**Italic** – コントロール内のテキストを斜体にするかどうかを指定します。

* **[画像の追加](control-add-picture.md)**、**[ボタン](control-button.md)**、**[チェック ボックス](control-check-box.md)**、**[日付の選択](control-date-picker.md)**、**[ドロップ ダウン](control-drop-down.md)**、**[エクスポート](control-export-import.md)**、**[インポート](control-export-import.md)**、**[ラベル](control-text-box.md)**、**[リスト ボックス](control-list-box.md)**、**[ラジオ](control-radio.md)**、**[テキスト入力](control-text-input.md)**、**[タイマー](control-timer.md)**の各コントロールに適用されます。

**Size** – コントロールに表示されるテキストのフォント サイズです。

* **[画像の追加](control-add-picture.md)**、**[ボタン](control-button.md)**、**[チェック ボックス](control-check-box.md)**、**[縦棒グラフ](control-column-line-chart.md)**、**[日付の選択](control-date-picker.md)**、**[ドロップ ダウン](control-drop-down.md)**、**[エクスポート](control-export-import.md)**、**[HTML テキスト](control-html-text.md)**、**[インポート](control-export-import.md)**、**[ラベル](control-text-box.md)**、**[折れ線グラフ](control-column-line-chart.md)**、**[リスト ボックス](control-list-box.md)**、**[ペン入力](control-pen-input.md)**、**[円グラフ](control-pie-chart.md)**、**[ラジオ](control-radio.md)**、**[テキスト入力](control-text-input.md)**、**[ライマー](control-timer.md)**の各コントロールに適用されます。

**Strikethrough** – コントロールに表示されるテキストに取り消し線を付けるかどうかを指定します。

* **[画像の追加](control-add-picture.md)**、**[ボタン](control-button.md)**、**[チェック ボックス](control-check-box.md)**、**[ドロップ ダウン](control-drop-down.md)**、**[エクスポート](control-export-import.md)**、**[インポート](control-export-import.md)**、**[ラベル](control-text-box.md)**、**[リスト ボックス](control-list-box.md)**、**[ラジオ](control-radio.md)**、**[テキスト入力](control-text-input.md)**、**[タイマー](control-timer.md)**の各コントロールに適用されます。

**Underline** – コントロールに表示されるテキストの下に線を引くかどうかを指定します。

* **[画像の追加](control-add-picture.md)**、**[ボタン](control-button.md)**、**[チェック ボックス](control-check-box.md)**、**[ドロップ ダウン](control-drop-down.md)**、**[エクスポート](control-export-import.md)**、**[インポート](control-export-import.md)**、**[ラベル](control-text-box.md)**、**[リスト ボックス](control-list-box.md)**、**[ラジオ](control-radio.md)**、**[テキスト入力](control-text-input.md)**、**[タイマー](control-timer.md)**の各コントロールに適用されます。

## <a name="text-placement"></a>テキストの配置
**Align** – コントロールの水平方向の中心に対するテキストの位置です。

* **[画像の追加](control-add-picture.md)**、**[ボタン](control-button.md)**、**[エクスポート](control-export-import.md)**、**[インポート](control-export-import.md)**、**[ラベル](control-text-box.md)**、**[ラジオ](control-radio.md)**、**[テキスト入力](control-text-input.md)**、**[タイマー](control-timer.md)**の各コントロールに適用されます。

**LineHeight** – テキストの行間やリスト内の項目間などの距離です。

* **[リスト ボックス](control-list-box.md)**、**[ラベル](control-text-box.md)**、**[ラジオ](control-radio.md)**、**[テキスト入力](control-text-input.md)**の各コントロールに適用されます。

**VerticalAlign** – コントロールの垂直方向の中心に対するコントロール上でのテキストの位置です。

* **[画像の追加](control-add-picture.md)**、**[ボタン](control-button.md)**、**[チェック ボックス](control-check-box.md)**、**[エクスポート](control-export-import.md)**、**[インポート](control-export-import.md)**、**[ラベル](control-text-box.md)**の各コントロールに適用されます。

