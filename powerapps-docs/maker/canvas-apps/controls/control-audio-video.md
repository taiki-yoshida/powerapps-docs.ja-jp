---
title: 'オーディオとビデオのコントロール: リファレンス | Microsoft Docs'
description: プロパティや例など、オーディオとビデオのコントロールに関する情報です
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
ms.openlocfilehash: 1661477ced59a678ac278dfcebe5e6f661c3e3f1
ms.sourcegitcommit: 59785e9e82da8f5bd459dcb5da3d5c18064b0899
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/22/2018
---
# <a name="audio-and-video-controls-in-powerapps"></a>PowerApps でのオーディオとビデオのコントロール
オーディオ ファイル、ビデオ ファイル、または YouTube のビデオを再生するコントロールです。

## <a name="description"></a>説明
**オーディオ** コントロールは、ファイルのサウンド クリップ、**[マイク](control-microphone.md)** コントロールからの録音、またはビデオ ファイルのオーディオ トラックを再生します。 **ビデオ** コントロールは、ファイルのビデオ クリップ、またはクローズド キャプション付き (省略可能) URL で指定された YouTube のビデオ クリップを再生します。

## <a name="key-properties"></a>主要なプロパティ
**Loop** – オーディオまたはビデオ クリップを、再生終了と同時に先頭から自動的に再開するかどうかを指定します。

**Media** - オーディオまたはビデオ コントロールが再生するクリップの ID です。

**ShowControls** – オーディオ プレイヤーまたはビデオ プレイヤーに再生ボタンと音量スライダーなどを表示するかどうか、およびペン コントロールに描画、削除、クリアなどのアイコンを表示するかどうかを指定します。

## <a name="additional-properties"></a>その他のプロパティ
**AutoPause** – ユーザーが別の画面に移動した場合、オーディオまたはビデオ クリップを自動的に一時停止するかどうかを指定します。

**AutoStart** – ユーザーがオーディオまたはビデオ コントロールを含む画面に移動したときに、自動的にクリップの再生を開始するかどうかを指定します。

**[BorderColor](properties-color-border.md)** – コントロールの境界線の色です。

**[BorderStyle](properties-color-border.md)** – コントロールの境界線を **Solid** (実線)、**Dashed** (破線)、**Dotted** (点線)、**None** (なし) のいずれに指定します。

**[BorderThickness](properties-color-border.md)** – コントロールの境界線の太さです。

**ClosedCaptionsUrl** – ビデオ コントロールのみ。  WebVTT 形式のクローズド キャプションのファイルの URL です。  ビデオの URL と キャプションの URL は、どちらも HTTPS である必要があります。 ビデオとキャプションの両方のファイルをホストするサーバーでは、CORS が有効になっている必要があります。

**[DisplayMode](properties-core.md)** – コントロールで、ユーザー入力を許可するか (**Edit**)、データの表示のみを許可するか (**View**)、許可しないか (**Disabled**) を設定します。

**[Fill](properties-color-border.md)** – コントロールの背景色です。

**[Height](properties-size-location.md)** – コントロールの上端と下端の距離です。

**[Image](properties-visual.md)** – イメージ、オーディオ、マイクの各コントロールに表示される画像の名前です。

**[ImagePosition](properties-visual.md)** – 画面またはコントロールのサイズが画像と異なる場合の、画面またはコントロール内の画像の位置です (**Fill** (フィル)、**Fit** (サイズに合わせる)、**Stretch** (伸ばす)、**Tile** (タイル表示)、または **Center** (中央に表示))。

**OnEnd** – オーディオまたはビデオ クリップの再生が終了したときの、アプリの応答方法です。

**OnPause** – オーディオまたはビデオ コントロールが再生しているクリップをユーザーが一時停止したときの、アプリの応答方法です。

**OnStart** – ユーザーがマイク コントロールで録音を開始したときの、アプリの応答方法です。

**Paused** – メディア再生コントロールが現在一時停止している場合は *true*、それ以外の場合は *false* です。

**[Reset](properties-core.md)** – コントロールを既定値に戻すかどうかを指定します。

**Start** – オーディオまたはビデオ クリップを再生するかどうかを指定します。

**StartTime** – クリップの再生が開始するとき、オーディオまたはビデオ クリップの開始後の時刻です。

**Time** – メディア コントロールの現在位置です。

**[Tooltip](properties-core.md)** – ポインターをコントロールに合わせたときに表示される説明テキストです。

**[Visible](properties-core.md)** – コントロールを表示するか非表示にするかを指定します。

**[Width](properties-size-location.md)** – コントロールの左端と右端の間の距離です。

**[X](properties-size-location.md)** – コントロールの左端とその親コンテナー (親コンテナーがない場合は画面) の左端間の距離です。

**[Y](properties-size-location.md)** – コントロールの上端とその親コンテナー (親コンテナーがない場合は画面) の上端間の距離です。

## <a name="related-functions"></a>関連する関数
[**First**( *TableName* )](../functions/function-first-last.md)

## <a name="examples"></a>例
### <a name="play-an-audio-or-video-file"></a>オーディオまたはビデオ ファイルを再生する
1. **[ファイル]** メニューの **[メディア]** をクリックまたはタップし、**[ビデオ]** または **[オーディオ]** をクリックまたはタップしてから、**[参照]** をクリックまたはタップします。
2. 再生するファイルを探してクリックまたはタップし、**[開く]** をクリックまたはタップします。
3. Esc キーを押して既定のワークスペースに戻り、**オーディオ**または**ビデオ** コントロールを追加して、**Media** プロパティを追加したファイルに設定します。

    [コントロールの追加および構成](../add-configure-controls.md)についてはこちらをご覧ください。
4. F5 キーを押し、追加したコントロールの再生ボタンをクリックまたはタップして、クリップを再生します。

    > [!TIP]
> **ビデオ** コントロールの再生ボタンは、コントロールをポイントすると表示されます。
5. Esc キーを押して既定のワークスペースに戻ります。

### <a name="play-a-youtube-video"></a>YouTube のビデオを再生する
1. **ビデオ** コントロールを追加し、**Media** プロパティに、YouTube のビデオの URL を二重引用符で囲んで設定します。
2. F5 キーを押し、**ビデオ** コントロールの再生ボタンをクリックまたはタップして、クリップを再生します。
3. Esc キーを押して既定のワークスペースに戻ります。
