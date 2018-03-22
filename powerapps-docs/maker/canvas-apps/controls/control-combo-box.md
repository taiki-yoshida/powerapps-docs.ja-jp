---
title: "コンボ ボックス コントロール: リファレンス | Microsoft Docs"
description: "各種プロパティとサンプルを含むコンボ ボックス コントロールに関する情報"
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
ms.date: 09/13/2017
ms.author: fikaradz
ms.openlocfilehash: 4d298e24ea967cbf5cb47638d4296f6efbd758c7
ms.sourcegitcommit: 6afca7cb4234d3a60111c5950e7855106ff97e56
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2018
---
# <a name="combo-box-control-in-powerapps"></a>PowerApps のコンボ ボックス コントロール
ユーザーが、提供された選択肢から選択できるようにするコントロール。  検索と複数選択をサポートしています。

## <a name="description"></a>説明
**コンボ ボックス**コントロールで、選択する項目を検索することができます。  検索は、SearchField プロパティについてサーバー側で実行されるので、パフォーマンスが非常に大規模なデータ ソースによって影響を受けることはありません。  

単一選択モードまたは複数選択モードは SelectMultiple プロパティを介して構成されます。

選択する項目を検索するとき、[データ] ウィンドウの [レイアウト] 設定を変更することで、項目ごとに、1 つのデータ値、2 つの値、または画像および 2 つの値 (Person) の表示を選択できます。

## <a name="people-picker"></a>メンバーの選択
**コンボ ボックス**をメンバーの選択に使用するには、[データ] ウィンドウの [レイアウト] 設定で **Person** テンプレートを選択し、メンバーの下に表示される関連データのプロパティを構成します。

## <a name="key-properties"></a>主要なプロパティ
**[項目](properties-core.md)** – 選択を行う元となるデータのソース。

**DefaultItems** – ユーザーがコントロールを操作する前に、最初に選択されている項目。

**SelectedItems** – ユーザーの操作の結果として得られる、選択されている項目の一覧。

**SelectMultiple** – ユーザーが、単一の項目を選択するか、複数の項目を選択するか。

**IsSearchable** – 選択する前にユーザーが項目を検索できるかどうか。

## <a name="additional-properties"></a>その他のプロパティ
**[BorderColor](properties-color-border.md)** – コントロールの境界線の色です。

**[BorderStyle](properties-color-border.md)** – コントロールの境界線を **Solid** (実線)、**Dashed** (破線)、**Dotted** (点線)、**None** (なし) のいずれに指定します。

**[BorderThickness](properties-color-border.md)** – コントロールの境界線の太さです。

**[Default](properties-core.md)** – 単一選択モードでユーザーが変更する前に、最初に選択されているもの。

**DisplayFields** – 検索によって返される各項目に対して表示されるフィールドの一覧。  プロパティの [オプション] タブで、データ ペインを使用して構成するのが最も簡単です。

**[DisplayMode](properties-core.md)** – コントロールで、ユーザー入力を許可するか (**Edit**)、データの表示のみを許可するか (**View**)、許可しないか (**Disabled**) を設定します。

**[Height](properties-size-location.md)** – コントロールの上端と下端の距離です。

**InputTextPlaceholder** – 項目が選択されていない場合、エンドユーザーに表示される指示テキスト。

**OnChange** – ユーザーが選択を変更したときのアプリの応答の仕方。

**OnNavigate** – ユーザーが項目をクリックしたときのアプリの応答の仕方。

**[OnSelect](properties-core.md)** – ユーザーがコントロールをタップまたはクリックした場合のアプリの反応を指定します。

**[Visible](properties-core.md)** – コントロールを表示するか非表示にするかを指定します。

**[Width](properties-size-location.md)** – コントロールの左端と右端の間の距離です。

**[X](properties-size-location.md)** – コントロールの左端とその親コンテナー (親コンテナーがない場合は画面) の左端間の距離です。

**[Y](properties-size-location.md)** – コントロールの上端とその親コンテナー (親コンテナーがない場合は画面) の上端間の距離です。

## <a name="example"></a>例
1. [コントロール] メニューの [挿入] タブから **[コンボ ボックス]** コントロールを追加します。  
2. プロパティの [オプション] タブで、[データ] をクリックします。  
3. データ ソース、レイアウトと以下の関連するプロパティを選択します。
4. [詳細設定] タブで **SelectMultiple** プロパティを設定します。

    機能**コンボ ボックス**がアプリに表示されます。

    [コントロールの追加および構成](../add-configure-controls.md)についてはこちらをご覧ください。
