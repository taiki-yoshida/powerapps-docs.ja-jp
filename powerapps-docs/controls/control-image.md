---
title: "イメージ コントロール: リファレンス | Microsoft Docs"
description: "各種プロパティとサンプルを含むイメージ コントロールに関する情報"
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
ms.openlocfilehash: 6266e8b59f19862e4b4a7f2364785da8e7547e73
ms.sourcegitcommit: 6afca7cb4234d3a60111c5950e7855106ff97e56
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2018
---
# <a name="image-control-in-powerapps"></a>PowerApps のイメージ コントロール
ローカル ファイルやデータ ソースの画像を表示するコントロールです。

## <a name="description"></a>説明
アプリに**イメージ** コントロールを 1 つまたは複数追加すると、データ セットに含まれていない個々の画像を表示したり、データ ソースのレコードの画像を組み合わせたりすることができます。

## <a name="key-properties"></a>主要なプロパティ
**[Image](properties-visual.md)** – イメージ、オーディオ、マイクの各コントロールに表示される画像の名前です。

## <a name="additional-properties"></a>その他のプロパティ
**ApplyEXIFOrientation** - 画像とともに埋め込まれたEXIF のデータで指定された向きを、自動的に適用するかどうかを指定します。

**AutoDisableOnSelect** – OnSelect の動作の実行時にコントロールを自動で無効化するかどうかを指定します。

**[BorderColor](properties-color-border.md)** – コントロールの境界線の色です。

**[BorderStyle](properties-color-border.md)** – コントロールの境界線を **Solid** (実線)、**Dashed** (破線)、**Dotted** (点線)、**None** (なし) のいずれに指定します。

**[BorderThickness](properties-color-border.md)** – コントロールの境界線の太さです。

**[FocusedBorderThickness](properties-color-border.md)** – キーボードでフォーカスした場合のコントロールの境界線の太さです。

**CalculateOriginalDimensions** – **OriginalHeight** プロパティと **OriginalWidth** プロパティを有効にします。

**[DisplayMode](properties-core.md)** – コントロールで、ユーザー入力を許可するか (**Edit**)、データの表示のみを許可するか (**View**)、許可しないか (**Disabled**) を設定します。

**[DisabledBorderColor](properties-color-border.md)** – コントロールの **[DisplayMode](properties-core.md)** プロパティが **Disabled** に設定されている場合のコントロールの境界線の色です。

**[DisabledFill](properties-color-border.md)** – コントロールの **[DisplayMode](properties-core.md)** プロパティが **Disabled** に設定されている場合のコントロールの背景色です。

**[Fill](properties-color-border.md)** – コントロールの背景色です。

**FlipHorizontal** - 画像を表示する前に水平方向に反転するかどうかを指定します。

**FlipVertical** - 画像を表示する前に垂直方向に反転するかどうかを指定します。

**[Height](properties-size-location.md)** – コントロールの上端と下端の距離です。

**[HoverBorderColor](properties-color-border.md)** – コントロール上にユーザーがマウス ポインターを重ねているときのコントロールの境界線の色です。

**[HoverFill](properties-color-border.md)** – コントロールにユーザーがマウス ポインターを重ねているときのコントロールの背景色です。

**[ImagePosition](properties-visual.md)** – 画面またはコントロールのサイズが画像と異なる場合の、画面またはコントロール内の画像の位置です (**Fill** (フィル)、**Fit** (サイズに合わせる)、**Stretch** (伸ばす)、**Tile** (タイル表示)、または **Center** (中央に表示))。

**ImageRotation** - 画像を表示する前に回転させる方法を指定します。  値には、なし、時計回り (CW) に 90 度、反時計回り (CCW) に 90 度、時計回りに 180 度を設定できます。

**[OnSelect](properties-core.md)** – ユーザーがコントロールをタップまたはクリックした場合のアプリの反応を指定します。

**OriginalHeight** – 画像の元の高さです。**CalculateOriginalDimensions** プロパティで有効にします。

**OriginalWidth** – 画像の元の幅です。**CalculateOriginalDimensions** プロパティで有効にします。

**[PaddingBottom](properties-size-location.md)** – コントロール内のテキストとそのコントロールの下端間の距離です。

**[PaddingLeft](properties-size-location.md)** – コントロール内のテキストとそのコントロールの左端間の距離です。

**[PaddingRight](properties-size-location.md)** – コントロール内のテキストとそのコントロールの右端間の距離です。

**[PaddingTop](properties-size-location.md)** – コントロール内のテキストとそのコントロールの上端間の距離です。

**[PressedBorderColor](properties-color-border.md)** – コントロールをユーザーがタップまたはクリックしたときのコントロールの境界線の色です。

**[PressedFill](properties-color-border.md)** – コントロールをユーザーがタップまたはクリックしたときのコントロールの背景色です。

**[RadiusBottomLeft](properties-size-location.md)** – コントロールの左下隅を丸める度合いです。

**[RadiusBottomRight](properties-size-location.md)** – コントロールの右下隅を丸める度合いです。

**[RadiusTopLeft](properties-size-location.md)** – コントロールの左上隅を丸める度合いです。

**[RadiusTopRight](properties-size-location.md)** – コントロールの右上隅を丸める度合いです。

**[Tooltip](properties-core.md)** – ポインターをコントロールに合わせたときに表示される説明テキストです。

**Transparency** – 画像の背後にあるコントロールを表示する度合いです。

**[Visible](properties-core.md)** – コントロールを表示するか非表示にするかを指定します。

**[Width](properties-size-location.md)** – コントロールの左端と右端の間の距離です。

**[X](properties-size-location.md)** – コントロールの左端とその親コンテナー (親コンテナーがない場合は画面) の左端間の距離です。

**[Y](properties-size-location.md)** – コントロールの上端とその親コンテナー (親コンテナーがない場合は画面) の上端間の距離です。

## <a name="related-functions"></a>関連する関数
[**Remove**( *DataSource*, ThisItem )](../functions/function-remove-removeif.md)

## <a name="examples"></a>例
### <a name="show-an-image-from-a-local-file"></a>ローカル ファイルの画像の表示
1. **[コンテンツ]** タブの **[メディア]** をクリックまたはタップして、**[参照]** をクリックまたはタップします。
2. 追加する画像ファイルをクリックまたはタップし、**[開く]** をクリックまたはタップしてから Esc キーを押して既定のワークスペースに戻ります。
3. **イメージ** コントロールを追加し、**[Items](properties-core.md)** プロパティを追加したファイルの名前に設定します。

    [コントロールの追加および構成](../add-configure-controls.md)についてはこちらをご覧ください。

    指定した画像が**イメージ** コントロールに表示されます。

### <a name="show-a-set-of-images-from-a-data-source"></a>データ ソースの画像セットの表示
1. こちらの [Excel ファイル](https://pwrappssamples.blob.core.windows.net/samples/FlooringEstimates.xlsx)をダウンロードして、ローカル デバイスに保存します。
2. PowerApps Studio で、アプリを作成するか開き、右のウィンドウで **[データ ソースの追加]** をクリックまたはタップします。

    右のウィンドウに **[データ ソースの追加]** が表示されない場合、左のナビゲーション バーの画面をどれかクリックまたはタップします。
3. **[静的データをアプリに追加します]** をクリックまたはタップして、ダウンロードした Excel ファイルをクリックまたはタップし、**[開く]** をクリックまたはタップします。
4. **[Flooring Estimates]** (フローリングの見積り) チェック ボックスをオンにして、**[接続]** をクリックまたはタップします。
5. **ギャラリー** コントロールと画像を追加し、**[Items](properties-core.md)** プロパティを **FlooringEstimates** に設定します。

    [コントロールの追加および構成](../add-configure-controls.md)についてはこちらをご覧ください。

    **ギャラリー** コントロールに、ダウンロードした Excel ファイルに含まれるリンクに基づくカーペット製品、硬木の製品、およびタイル製品の画像が表示されます。
