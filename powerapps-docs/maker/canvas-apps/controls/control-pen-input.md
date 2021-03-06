---
title: 'ペン入力コントロール: リファレンス | Microsoft Docs'
description: 各種プロパティとサンプルを含むペン入力コントロールに関する情報
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
ms.openlocfilehash: 7e5be9b68b501279329c23f9afe5d451487fa8d1
ms.sourcegitcommit: 59785e9e82da8f5bd459dcb5da3d5c18064b0899
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/22/2018
---
# <a name="pen-input-control-in-powerapps"></a>PowerApps のペン入力コントロール
ユーザーが画像の領域を描画、削除、強調表示できるコントロールです。

## <a name="description"></a>説明
ユーザーはこのコントロールをホワイトボードのように使用して、図を描いたり、入力テキストに変換可能な文字を書いたりすることができます。

## <a name="key-properties"></a>主要なプロパティ
**[Color](properties-color-border.md)** – 入力ストロークの色です。

**Mode** – このコントロールのモードは **Draw** (描画) または **Erase** (削除) です。  Select (選択) モードは廃止されました。

## <a name="additional-properties"></a>その他のプロパティ
**[BorderColor](properties-color-border.md)** – コントロールの境界線の色です。

**[BorderStyle](properties-color-border.md)** – コントロールの境界線を **Solid** (実線)、**Dashed** (破線)、**Dotted** (点線)、**None** (なし) のいずれに指定します。

**[BorderThickness](properties-color-border.md)** – コントロールの境界線の太さです。

**[DisplayMode](properties-core.md)** – コントロールで、ユーザー入力を許可するか (**Edit**)、データの表示のみを許可するか (**View**)、許可しないか (**Disabled**) を設定します。

**[Fill](properties-color-border.md)** – コントロールの背景色です。

**[Height](properties-size-location.md)** – コントロールの上端と下端の距離です。

**Input** – 入力です。

**[OnSelect](properties-core.md)** – ユーザーがコントロールをタップまたはクリックした場合のアプリの反応を指定します。

**[SelectionColor](properties-color-border.md)** – リスト内で選択された項目のテキストの色、またはペン コントロールの選択ツールの色です。

**SelectionThickness** – ペン入力コントロールの選択ツールの太さです。

**ShowControls** – オーディオ プレイヤーまたはビデオ プレイヤーに再生ボタンと音量スライダーなどを表示するかどうか、およびペン コントロールに描画、削除、クリアなどのアイコンを表示するかどうかを指定します。

**[Size](properties-text.md)** – コントロールに表示されるテキストのフォント サイズです。

**[Tooltip](properties-core.md)** – ポインターをコントロールに合わせたときに表示される説明テキストです。

**[Visible](properties-core.md)** – コントロールを表示するか非表示にするかを指定します。

**[Width](properties-size-location.md)** – コントロールの左端と右端の間の距離です。

**[X](properties-size-location.md)** – コントロールの左端とその親コンテナー (親コンテナーがない場合は画面) の左端間の距離です。

**[Y](properties-size-location.md)** – コントロールの上端とその親コンテナー (親コンテナーがない場合は画面) の上端間の距離です。

## <a name="related-functions"></a>関連する関数
[**Collect**( *CollectionName*, *DatatoCollect* )](../functions/function-clear-collect-clearcollect.md)

## <a name="example"></a>例
### <a name="create-a-set-of-images"></a>画像セットの作成
1. **ペン入力**コントロールを追加して **MyDoodles** という名前を付け、**ShowControls** プロパティを **true** に設定します。
   
    [コントロールの追加、命名、構成についてはこちらをご覧ください](../add-configure-controls.md)。
2. **[ボタン](control-button.md)** コントロールを追加して **MyDoodles** の下に移動し、**[ボタン](control-button.md)** コントロールの **[Text](properties-core.md)** プロパティを、**Add** (追加) と表示するように設定します。
3. **[ボタン](control-button.md)** コントロールの **[OnSelect](properties-core.md)** プロパティに次の式を設定します。<br>
   **Collect(Doodles, {Sketch:MyDoodles.Image})**
4. **イメージ ギャラリー** コントロールを追加して**[ボタン](control-button.md)** コントロールの下に移動させ、**イメージ ギャラリー**の幅を表示項目が 3 つになるまで縮小します。
5. **イメージ ギャラリー** コントロールの **[Items](properties-core.md)** プロパティを **[Doodles]** に設定し、F5 キーを押します。
6. **MyDoodles** に絵を描いてから、**[ボタン](control-button.md)** コントロールをクリックまたはタップします。
   
    描いた絵が、**イメージ ギャラリー** コントロールに表示されます。
7. (省略可能) **ペン入力** コントロール内で描いた絵を消去するアイコンをクリックまたはタップし、別の絵を描いてから、**[ボタン](control-button.md)** コントロールをクリックまたはタップします。
8. **イメージ ギャラリー** コントロール内で、**[イメージ](control-image.md)** コントロールの  **[OnSelect](properties-core.md)** プロパティに次の式を設定します。<br>
   **Remove(Doodles, ThisItem)**
9. **イメージ ギャラリー** コントロール内の絵をクリックまたはタップすると、その絵を削除できます。

**[SaveData](../functions/function-savedata-loaddata.md)** 関数を使用して絵をローカルに保存するか、**[Patch](../functions/function-patch.md)** 関数を使用してデータ ソースに保存します。

