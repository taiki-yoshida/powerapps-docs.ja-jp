---
title: "スクリーン コントロール: リファレンス | Microsoft Docs"
description: "各種プロパティとサンプルを含む画面コントロールに関する情報"
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
ms.openlocfilehash: d9b1251d27fc45fd4ad13fd401d2e13c7390f26c
ms.sourcegitcommit: 43be6a4e08849d522aabb6f767a81c092419babc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2017
---
# <a name="screen-control-in-powerapps"></a>PowerApps の画面コントロール
アプリ内で 1 つまたは複数の他のコントロールを含む UI 要素。

## <a name="description"></a>説明
ほとんどのアプリには、**[ラベル](control-text-box.md)** コントロールや**[ボタン](control-button.md)** コントロールのほか、データを表示したりナビゲーションをサポートしたりするその他のコントロールを含む複数の**画面**コントロールがあります。

## <a name="key-properties"></a>主要なプロパティ
**[BackgroundImage](properties-visual.md)** – 画面の背景に表示される画像ファイルの名前です。

**[Fill](properties-color-border.md)** – コントロールの背景色です。

## <a name="additional-properties"></a>その他のプロパティ
**[ImagePosition](properties-visual.md)** – 画面またはコントロールのサイズが画像と異なる場合の、画面またはコントロール内の画像の位置です (**Fill** (フィル)、**Fit** (サイズに合わせる)、**Stretch** (伸ばす)、**Tile** (タイル表示)、または **Center** (中央に表示))。

**OnHidden** – ユーザーがある画面から離れたときのアプリの動作。

**OnVisible** – ユーザーが画面に移動したときのアプリの動作。

**OnStart** – ユーザーがアプリを開くときのアプリの動作です。

* このプロパティで設定した数式は、アプリの最初の画面が表示される前に実行されます。 アプリ開始時にどの画面が最初に表示されるかを変更するには、[**Navigate**](../functions/function-navigate.md) 関数を呼び出します。
* [**UpdateContext**](../functions/function-updatecontext.md) 関数で[コンテキスト変数](../workding-with-variables.md)を設定することはできません (どの画面もまだ表示されていないため)。 ただし、**Navigate** 関数でコンテキスト変数を渡し、[**Collect**](../functions/function-collect.md) 関数を使用して[コレクション](../workding-with-variables.md)を作成し、そのコレクションに入力することができます。
* アプリを更新する場合、このプロパティで設定した数式は、アプリが PowerApps Studio に読み込まれるときに実行されます。 このプロパティ変更の影響を確認するには、アプリを保存して閉じ、再読み込みする必要があります。
* **OnStart** プロパティは、実際には画面ではなくアプリのプロパティです。 編集の便宜を考慮して、このプロパティをアプリの最初の画面のプロパティとして表示し、変更します。 最初の画面を削除したか、画面の順序を変更したために、このプロパティを見つけられなくなることがあります。 その場合は、アプリを保存して閉じ、再読み込みすると、最初の画面のプロパティとして表示されます。

## <a name="related-functions"></a>関連する関数
[**Distinct**( *DataSource*, *ColumnName* )](../functions/function-distinct.md)

## <a name="example"></a>例
1. **[ラジオ](control-radio.md)** コントロールを追加して **ScreenFills** という名前を付け、その **[Items](properties-core.md)** プロパティを次の値に設定します。<br>
   **["Red", "Green"]**
   
    [コントロールの追加、命名、構成についてはこちらをご覧ください](../add-configure-controls.md)。
2. 既定の**画面**コントロールに**Source** という名前を付け、別の**画面**コントロールを追加して **Target** という名前を付けます。
3. **Source** に **[シェイプ](control-shapes-icons.md)** コントロール (矢印など) を追加し、その **[OnSelect](properties-core.md)** プロパティを次の数式に設定します。<br>
   **Navigate(Target, ScreenTransition.Fade)**
   
    **[Navigate](../functions/function-navigate.md)** 関数または[その他の関数](../formula-reference.md)については各関連記事を参照してください。
4. **Target** に **[シェイプ](control-shapes-icons.md)** コントロール (矢印など) を追加し、その **[OnSelect](properties-core.md)** プロパティを次の数式に設定します。<br>
   **Navigate(Source, ScreenTransition.Fade)**
5. **Target** の **[Fill](properties-color-border.md)** プロパティを次の数式に設定します。<br>
   **If("Red" in ScreenFills.Selected.Value, RGBA(255, 0, 0, 1), RGBA(54, 176, 75, 1))**
6. **Source** から、F5 キーを押して、**[ラジオ](control-radio.md)** コントロールのどちらかのオプションをクリックまたはタップしてから、**[シェイプ](control-shapes-icons.md)** コントロールをクリックまたはタップします。
   
    **Target** が、選択した色で表示されます。
7. **Target** で、**[シェイプ](control-shapes-icons.md)** コントロールをクリックまたはタップして **Source** に戻ります。
8. (オプション) **[ラジオ](control-radio.md)** コントロールの他のオプションをクリックまたはタップしてから、**[シェイプ](control-shapes-icons.md)** コントロールをクリックまたはタップして **Target** が他の色で表示されることを確認します。
9. 既定のワークスペースに戻るには、Esc キーを押します。

