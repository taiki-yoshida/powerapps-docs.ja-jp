---
title: "バーコード スキャナー コントロール: リファレンス | Microsoft Docs"
description: "各種プロパティとサンプルを含むバーコード スキャナー コントロールに関する情報"
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
ms.openlocfilehash: c27a2319d74db9a50acff84e40ea7df83dc1c126
ms.sourcegitcommit: 33099e6197c0139679cd08c42e9e2a5717904c92
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/12/2018
---
# <a name="barcode-scanner-control-in-powerapps"></a>PowerApps のバーコード スキャナー コントロール
デバイスのバーコード スキャナーを使って写真を撮影できるコントロールです。

## <a name="description"></a>説明
このコントロールを追加した場合、ユーザーは、アプリを実行している任意の場所から 1 枚以上の写真でデータ ソースを更新できます。

## <a name="key-properties"></a>主要なプロパティ
**barcode scanner** – 複数のバーコード スキャナーを備えるデバイスで、アプリが使うバーコード スキャナーの数値 ID です。

## <a name="additional-properties"></a>その他のプロパティ
**[BorderColor](properties-color-border.md)** – コントロールの境界線の色です。

**[BorderStyle](properties-color-border.md)** – コントロールの境界線を **Solid** (実線)、**Dashed** (破線)、**Dotted** (点線)、**None** (なし) のいずれに指定します。

**[BorderThickness](properties-color-border.md)** – コントロールの境界線の太さです。

**Brightness** – ユーザーが画像で認識する可能性のある光の量を指定します。

**Contrast** – ユーザーが画像内の似た色をどれだけ容易に区別できるかを指定します。

**[DisplayMode](properties-core.md)** – コントロールで、ユーザー入力を許可するか (**Edit**)、データの表示のみを許可するか (**View**)、許可しないか (**Disabled**) を設定します。

**[Height](properties-size-location.md)** – コントロールの上端と下端の距離です。

**[OnSelect](properties-core.md)** – ユーザーがコントロールをタップまたはクリックした場合のアプリの反応を指定します。

**OnStream** – **Stream** プロパティが更新された場合のアプリの反応を指定します。

**Photo** – ユーザーが写真を撮影すると取得される画像です。

**Stream** – **StreamRate** プロパティに基づいて自動的に更新された画像です。

**StreamRate** – **Stream** プロパティの画像を更新する頻度です (ミリ秒単位)。  この値の範囲は、100 (0.1 秒) から 3,600,000 (1 時間) です。

**[Tooltip](properties-core.md)** – ポインターをコントロールに合わせたときに表示される説明テキストです。

**[Visible](properties-core.md)** – コントロールを表示するか非表示にするかを指定します。

**[Width](properties-size-location.md)** – コントロールの左端と右端の間の距離です。

**[X](properties-size-location.md)** – コントロールの左端とその親コンテナー (親コンテナーがない場合は画面) の左端間の距離です。

**[Y](properties-size-location.md)** – コントロールの上端とその親コンテナー (親コンテナーがない場合は画面) の上端間の距離です。

**Zoom** – バーコード スキャナーからの画像、または PDF ビューアーでのファイルの表示を拡大する割合です。

## <a name="related-functions"></a>関連する関数
[**Patch**( *DataSource*, *BaseRecord*, *ChangeRecord* )](../functions/function-patch.md)

## <a name="example"></a>例
### <a name="add-photos-to-an-image-gallery-control"></a>イメージ ギャラリー コントロールに写真を追加する
1. **バーコード スキャナー** コントロールを追加し、名前を **Mybarcode scanner** に設定します
   
    [コントロールの追加、命名、構成についてはこちらをご覧ください](../add-configure-controls.md)。
2. **ラベル** コントロールを追加し、その出力をバーコードの値に設定します。  
3. BarcodeType プロパティで設定されている種類のバーコードをスキャンします。
4. スキャンされたバーコードがラベルに表示されます。

