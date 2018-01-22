---
title: "画像の追加コントロール: リファレンス | Microsoft Docs"
description: "各種プロパティとサンプルを含む画像の追加コントロールに関する情報"
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
ms.openlocfilehash: 6a7c60755f5623803d20bec4ec9881108b1116c6
ms.sourcegitcommit: 33099e6197c0139679cd08c42e9e2a5717904c92
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/12/2018
---
# <a name="add-picture-control-in-powerapps"></a>PowerApps の画像の追加コントロール
写真を撮影したり、ローカルのデバイスから画像を読み込んだりします。

## <a name="description"></a>説明
このコントロールを使用すると、ユーザーは写真を撮影したり、デバイスから画像ファイルをアップロードしたりして、このコンテンツでデータ ソースを更新できます。 モバイル デバイスでは、デバイスの選択ダイアログが表示され、ユーザーは写真を撮影するか、既存の画像を使用するかを選択できます。

このコントロールは、2 つのコントロールで構成される複合コントロールです。  読み込まれた画像を表示する外側のコントロールを選択するには、1 回押すかタップします。  内側のテキスト ボックス コントロールを選択するには、もう一度押すかタップします。

## <a name="outer-control-properties"></a>外側のコントロールのプロパティ
これらのプロパティは、外側のコントロールに適用されます。

**[BorderColor](properties-color-border.md)** – コントロールの境界線の色です。

**[BorderStyle](properties-color-border.md)** – コントロールの境界線を **Solid** (実線)、**Dashed** (破線)、**Dotted** (点線)、**None** (なし) のいずれに指定します。

**[BorderThickness](properties-color-border.md)** – コントロールの境界線の太さです。

**[DisplayMode](properties-core.md)** – コントロールで、ユーザー入力を許可するか (**Edit**)、データの表示のみを許可するか (**View**)、許可しないか (**Disabled**) を設定します。

**[DisabledBorderColor](properties-color-border.md)** – コントロールの **[DisplayMode](properties-core.md)** プロパティが **Disabled** に設定されている場合のコントロールの境界線の色です。

**[DisabledFill](properties-color-border.md)** – コントロールの **[DisplayMode](properties-core.md)** プロパティが **Disabled** に設定されている場合のコントロールの背景色です。

**Error** - 画像のアップロードで問題が発生した場合、このプロパティには該当するエラー文字列が含まれます。

**[Fill](properties-color-border.md)** – コントロールの背景色です。

**[Height](properties-size-location.md)** – コントロールの上端と下端の距離です。

**[HoverBorderColor](properties-color-border.md)** – コントロール上にユーザーがマウス ポインターを重ねているときのコントロールの境界線の色です。

**[HoverFill](properties-color-border.md)** – コントロールにユーザーがマウス ポインターを重ねているときのコントロールの背景色です。

**Media** – オーディオまたはビデオ コントロールが再生するクリップの ID です。

**[OnSelect](properties-core.md)** – ユーザーがコントロールをタップまたはクリックした場合のアプリの反応を指定します。

**[PressedBorderColor](properties-color-border.md)** – コントロールをユーザーがタップまたはクリックしたときのコントロールの境界線の色です。

**[PressedFill](properties-color-border.md)** – コントロールをユーザーがタップまたはクリックしたときのコントロールの背景色です。

**[Visible](properties-core.md)** – コントロールを表示するか非表示にするかを指定します。

**[Width](properties-size-location.md)** – コントロールの左端と右端の間の距離です。

**[X](properties-size-location.md)** – コントロールの左端とその親コンテナー (親コンテナーがない場合は画面) の左端間の距離です。

**[Y](properties-size-location.md)** – コントロールの上端とその親コンテナー (親コンテナーがない場合は画面) の上端間の距離です。

## <a name="inner-text-properties"></a>内側のテキストのプロパティ
これらのプロパティは、既定では "画像を追加するにはタップまたはクリックしてください" と表示されている内側のラベル コントロールに適用されます。  この内側のコントロールを選択するには、**画像の追加**コントロールを 1 回押すかタップしてから、もう一度押すかタップします。

**[Align](properties-text.md)** – コントロールの水平方向の中心に対するテキストの位置です。

**[Color](properties-color-border.md)** – コントロールのテキストの色です。

**[DisabledColor](properties-color-border.md)** – コントロールの **[DisplayMode](properties-core.md)** プロパティが **Disabled** に設定されている場合のコントロール内のテキストの色です。

**[Font](properties-text.md)** – テキストを表記するフォントのファミリー名です。

**[FontWeight](properties-text.md)** – コントロール内のテキストの太さです。**Bold** (太字)、**Semibold** (中太)、**Normal** (標準)、**Lighter** (細字) から指定します。

**[HoverColor](properties-color-border.md)** – コントロールにユーザーがマウス ポインターを重ねているときのコントロール内のテキストの色です。

**[Italic](properties-text.md)** – コントロール内のテキストを斜体にするかどうかを指定します。

**[OnChange](properties-core.md)** – ユーザーが (スライダーを調整するなどして) コントロールの値を変更した場合のアプリの反応を指定します。

**[Padding](properties-size-location.md)** – [インポート] ボタンまたは [エクスポート] ボタンのテキストと、ボタンの縁との距離です。

**[PressedColor](properties-color-border.md)** – コントロールをユーザーがタップまたはクリックしたときのコントロール内のテキストの色です。

**[Size](properties-text.md)** – コントロールに表示されるテキストのフォント サイズです。

**[Strikethrough](properties-text.md)** – コントロールに表示されるテキストに取り消し線を付けるかどうかを指定します。

**[Text](properties-core.md)** – コントロールに表示されるテキスト、またはコントロールにユーザーが入力するテキストです。

**[Underline](properties-text.md)** – コントロールに表示されるテキストの下に線を引くかどうかを指定します。

**[VerticalAlign](properties-text.md)** – コントロールの垂直方向の中心に対するコントロール上でのテキストの位置です。

## <a name="related-functions"></a>関連する関数
[**Patch**( *DataSource*, *BaseRecord*, *ChangeRecord* )](../functions/function-patch.md)

## <a name="example"></a>例
### <a name="add-images-to-an-image-gallery-control"></a>イメージ ギャラリー コントロールへの画像の追加
1. **画像の追加**コントロールを追加し、それをトリプル クリックします。
   
    [コントロールの追加、命名、構成についてはこちらをご覧ください](../add-configure-controls.md)。
2. **[Open (開く)]** ダイアログ ボックスで、画像ファイルをクリックまたはタップしてから、**[Open (開く)]** をクリックまたはタップします。
3. **[ボタン](control-button.md)** コントロールを追加して**画像の追加**コントロールの下に移動し、**[ボタン](control-button.md)** コントロールの **[OnSelect](properties-core.md)** プロパティを次の数式に設定します。<br>
   **Collect(MyPix, AddMediaButton1.Media)**
   
    **[Collect](../functions/function-clear-collect-clearcollect.md)** 関数または[その他の関数](../formula-reference.md)については各関連記事を参照してください。
4. **イメージ ギャラリー** コントロールを追加し、その **[Items](properties-core.md)** プロパティを **MyPix** に設定します。
5. F5 キーを押して、**[ボタン](control-button.md)** コントロールをクリックまたはタップします。
   
    **画像の追加**コントロールの画像が**イメージ ギャラリー** コントロールに表示されます。 画像の縦横比が**イメージ ギャラリー** コントロール内の**[イメージ](control-image.md)** コントロールと同じでない場合は、**[イメージ](control-image.md)** コントロールの **[ImagePosition](properties-visual.md)** プロパティを **Fit** に設定します。
6. **画像の追加**コントロールをクリックまたはタップし、別の画像ファイルをクリックまたはタップし、**[Open (開く)]** をクリックまたはタップしてから、追加した**[ボタン](control-button.md)** コントロールをクリックまたはタップします。
   
    2 番目の画像が**イメージ ギャラリー** コントロールに表示されます。
7. (オプション) 前の手順を 1 回以上繰り返してから、Esc キーを押して既定のワークスペースに戻ります。

**[SaveData](../functions/function-savedata-loaddata.md)** 関数を使用して画像をローカルに保存するか、**[Patch](../functions/function-patch.md)** 関数を使用してデータ ソースを更新します。

