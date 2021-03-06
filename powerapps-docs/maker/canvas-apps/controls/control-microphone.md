---
title: 'マイク コントロール: リファレンス | Microsoft Docs'
description: 各種プロパティとサンプルを含むマイク コントロールに関する情報
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
ms.openlocfilehash: 3ffede0018a371b3c3a4cf4a3a1f9fc8115140de
ms.sourcegitcommit: 59785e9e82da8f5bd459dcb5da3d5c18064b0899
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/22/2018
---
# <a name="microphone-control-in-powerapps"></a>PowerApps のマイク コントロール
ユーザーがサウンドを録音できるコントロールです。

## <a name="description"></a>説明
このコントロールを追加した場合、ユーザーは、アプリを実行している任意の場所から 1 つ以上のサウンドでデータ ソースを更新できます。

## <a name="key-properties"></a>主要なプロパティ
**Mic** – 複数のマイクを備えたデバイスでの、アプリが使用するマイクの数値 ID です。

**OnStop** – ユーザーがマイク コントロールで録音を終了したときの、アプリの応答方法です。

## <a name="additional-properties"></a>その他のプロパティ
**[BorderColor](properties-color-border.md)** – コントロールの境界線の色です。

**[BorderStyle](properties-color-border.md)** – コントロールの境界線を **Solid** (実線)、**Dashed** (破線)、**Dotted** (点線)、**None** (なし) のいずれに指定します。

**[BorderThickness](properties-color-border.md)** – コントロールの境界線の太さです。

**[Color](properties-color-border.md)** – コントロールのテキストの色です。

**[DisplayMode](properties-core.md)** – コントロールで、ユーザー入力を許可するか (**Edit**)、データの表示のみを許可するか (**View**)、許可しないか (**Disabled**) を設定します。

**[DisabledBorderColor](properties-color-border.md)** – コントロールの **[DisplayMode](properties-core.md)** プロパティが **Disabled** に設定されている場合のコントロールの境界線の色です。

**[DisabledColor](properties-color-border.md)** – コントロールの **[DisplayMode](properties-core.md)** プロパティが **Disabled** に設定されている場合のコントロール内のテキストの色です。

**[DisabledFill](properties-color-border.md)** – コントロールの **[DisplayMode](properties-core.md)** プロパティが **Disabled** に設定されている場合のコントロールの背景色です。

**[Fill](properties-color-border.md)** – コントロールの背景色です。

**[Height](properties-size-location.md)** – コントロールの上端と下端の距離です。

**[HoverBorderColor](properties-color-border.md)** – コントロール上にユーザーがマウス ポインターを重ねているときのコントロールの境界線の色です。

**[HoverColor](properties-color-border.md)** – コントロールにユーザーがマウス ポインターを重ねているときのコントロール内のテキストの色です。

**[HoverFill](properties-color-border.md)** – コントロールにユーザーがマウス ポインターを重ねているときのコントロールの背景色です。

**[Image](properties-visual.md)** – イメージ、オーディオ、マイクの各コントロールに表示される画像の名前です。

**[ImagePosition](properties-visual.md)** – 画面またはコントロールのサイズが画像と異なる場合の、画面またはコントロール内の画像の位置です (**Fill** (フィル)、**Fit** (サイズに合わせる)、**Stretch** (伸ばす)、**Tile** (タイル表示)、または **Center** (中央に表示))。

**[OnSelect](properties-core.md)** – ユーザーがコントロールをタップまたはクリックした場合のアプリの反応を指定します。

**OnStart** – ユーザーがマイク コントロールで録音を開始したときの、アプリの応答方法です。

**[PressedBorderColor](properties-color-border.md)** – コントロールをユーザーがタップまたはクリックしたときのコントロールの境界線の色です。

**[PressedColor](properties-color-border.md)** – コントロールをユーザーがタップまたはクリックしたときのコントロール内のテキストの色です。

**[PressedFill](properties-color-border.md)** – コントロールをユーザーがタップまたはクリックしたときのコントロールの背景色です。

**[Reset](properties-core.md)** – コントロールを既定値に戻すかどうかを指定します。

**[Tooltip](properties-core.md)** – ポインターをコントロールに合わせたときに表示される説明テキストです。

**[Visible](properties-core.md)** – コントロールを表示するか非表示にするかを指定します。

**[Width](properties-size-location.md)** – コントロールの左端と右端の間の距離です。

**[X](properties-size-location.md)** – コントロールの左端とその親コンテナー (親コンテナーがない場合は画面) の左端間の距離です。

**[Y](properties-size-location.md)** – コントロールの上端とその親コンテナー (親コンテナーがない場合は画面) の上端間の距離です。

## <a name="related-functions"></a>関連する関数
[**Patch**( *DataSource*, *BaseRecord*, *ChangeRecord* )](../functions/function-patch.md)

## <a name="example"></a>例
### <a name="add-sounds-to-a-custom-gallery-control"></a>カスタム ギャラリー コントロールにサウンドを追加します。
1. **マイク**を追加し、「**MyMic**」という名前を付け、**OnStop** プロパティに次の数式を設定します。<br>
   **Collect(MySounds, MyMic.Audio)**
   
    [コントロールの追加、命名、構成についてはこちらをご覧ください](../add-configure-controls.md)。
   
    **[Collect](../functions/function-clear-collect-clearcollect.md)** 関数または[その他の関数](../formula-reference.md)については各関連記事を参照してください。
2. **カスタム ギャラリー** コントロールを追加し、**MyMic** の下に移動し、**カスタム ギャラリー** コントロールの **[Items](properties-core.md)** プロパティを **MySounds** に設定します。
3. **カスタム ギャラリー** コントロール用のテンプレートで、**[オーディオ](control-audio-video.md)** コントロールを追加し、**Media** プロパティを **ThisItem.Url** に設定します。
4. F5 キーを押して、**MyMic** をクリックまたはタップして録音を開始し、もう一度クリックまたはタップして録音を停止します。
5. **カスタム ギャラリー** コントロールで、**[オーディオ](control-audio-video.md)** コントロールの再生ボタンをクリックまたはタップして録音を再生します。
6. 必要な数のサウンドを録音してから、Esc キーを押して既定のワークスペースに戻ります。
7. (省略可能) **カスタム ギャラリー** コントロール用のテンプレートで、**[ボタン](control-button.md)** コントロールを追加し、**[OnSelect](properties-core.md)** プロパティを **Remove(MySounds, ThisItem)** に設定し、F5 キーを押してから、**ボタン** コントロールをクリックまたはタップして対応する録音を削除します。

**[SaveData](../functions/function-savedata-loaddata.md)** 関数を使用して録音をローカルに保存するか、**[Patch](../functions/function-patch.md)** 関数を使用してデータ ソースを更新します。

