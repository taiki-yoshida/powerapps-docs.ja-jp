---
title: "カメラ コントロール: リファレンス | Microsoft Docs"
description: "各種プロパティとサンプルを含むカメラ コントロールに関する情報"
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
ms.openlocfilehash: a3a724ad42082962ec8aea4e616f1d75aa7299ec
ms.sourcegitcommit: 33099e6197c0139679cd08c42e9e2a5717904c92
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/12/2018
---
# <a name="camera-control-in-powerapps"></a>PowerApps のカメラ コントロール
ユーザーがデバイスのカメラを使って写真を撮影するために使用できるコントロールです。

## <a name="description"></a>説明
このコントロールを追加した場合、ユーザーは、アプリを実行している任意の場所から 1 枚以上の写真でデータ ソースを更新できます。

## <a name="key-properties"></a>主要なプロパティ
**Camera** – 複数のカメラを備えたデバイスでの、アプリが使用するカメラの数値 ID です。

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

**Zoom** – カメラからの画像、または PDF ビューアーでのファイルの表示を拡大する割合です。

## <a name="related-functions"></a>関連する関数
[**Patch**( *DataSource*, *BaseRecord*, *ChangeRecord* )](../functions/function-patch.md)

## <a name="example"></a>例
### <a name="add-photos-to-an-image-gallery-control"></a>イメージ ギャラリー コントロールに写真を追加する
1. **Camera** コントロールを追加して **MyCamera** という名前を付け、その **[OnSelect](properties-core.md)** プロパティを次の数式に設定します。<br>
   **Collect(MyPix, MyCamera.Photo)**
   
    [コントロールの追加、命名、構成についてはこちらをご覧ください](../add-configure-controls.md)。
   
    **[Collect](../functions/function-clear-collect-clearcollect.md)** 関数または[その他の関数](../formula-reference.md)については各関連記事を参照してください。
2. F5 キーを押した後、**MyCamera** をクリックまたはタップして写真を撮影します。
3. **[イメージ ギャラリー コントロール](control-gallery.md)**を追加してから、その**[イメージ](control-image.md)** コントロール、テンプレート、さらに**イメージ ギャラリー** コントロール自体のサイズを画面内に収まるように変更します。
4. **画像ギャラリー** コントロールの **[Items](properties-core.md)** プロパティを次の式に設定します。<br>**MyPix.Url**
5. ギャラリーで、**画像**コントロールの **[Image](properties-visual.md)** プロパティを次の式に設定します。<br>
   **ThisItem.Url**
   
    撮影した写真が**イメージ ギャラリー** コントロールに表示されます。
6. 必要な枚数の写真を撮影してから、Esc キーを押して既定のワークスペースに戻ります。
7. (省略可能) **イメージ ギャラリー** コントロール内の**イメージ** コントロールの **OnSelect** プロパティを **Remove(MyPix, ThisItem)** に設定し、F5 キーを押して、写真をクリックまたはタップして削除します。

**[SaveData](../functions/function-savedata-loaddata.md)** 関数を使用して写真をローカルに保存するか、**[Patch](../functions/function-patch.md)** 関数を使用してデータ ソースを更新します。

