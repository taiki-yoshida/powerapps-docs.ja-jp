---
title: "縦棒グラフ コントロールと折れ線グラフ コントロール: リファレンス | Microsoft Docs"
description: "各種プロパティとサンプルを含む縦棒グラフ コントロールと折れ線グラフ コントロールに関する情報"
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
ms.openlocfilehash: 039b267394ef6be5e3038fa0b07149f69fee6a51
ms.sourcegitcommit: 33099e6197c0139679cd08c42e9e2a5717904c92
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/12/2018
---
# <a name="column-chart-and-line-chart-controls-in-powerapps"></a>PowerApps での縦棒グラフ コントロールと折れ線グラフ コントロール
X 軸と Y 軸からなるグラフとしてデータを表示するコントロールです。

## <a name="description"></a>説明
既定では、**縦棒グラフ** コントロールまたは**折れ線グラフ** コントロールは、グループ化された複数のコントロールで構成されます。 これらのコントロールには、タイトル、データ、凡例が表示されます。

## <a name="key-properties"></a>主要なプロパティ
**[Items](properties-core.md)** – ギャラリー、リスト、グラフなどのコントロールに表示されるデータのソースです。

**NumberOfSeries** – 縦棒グラフまたは折れ線グラフに反映されるデータ列の数です。

## <a name="all-properties"></a>すべてのプロパティ
**[BorderColor](properties-color-border.md)** – コントロールの境界線の色です。

**[BorderStyle](properties-color-border.md)** – コントロールの境界線を **Solid** (実線)、**Dashed** (破線)、**Dotted** (点線)、**None** (なし) のいずれに指定します。

**[BorderThickness](properties-color-border.md)** – コントロールの境界線の太さです。

**[Color](properties-color-border.md)** – コントロールのテキストの色です。

**[DisplayMode](properties-core.md)** – コントロールで、ユーザー入力を許可するか (**Edit**)、データの表示のみを許可するか (**View**)、許可しないか (**Disabled**) を設定します。

**[DisabledBorderColor](properties-color-border.md)** – コントロールの **[DisplayMode](properties-core.md)** プロパティが **Disabled** に設定されている場合のコントロールの境界線の色です。

**[Font](properties-text.md)** – テキストを表記するフォントのファミリー名です。

**GridStyle** – 縦棒グラフまたは折れ線グラフで、X 軸と Y 軸のどちらか一方または両方を表示するか、または両方とも表示しないかを指定します。

**[Height](properties-size-location.md)** – コントロールの上端と下端の距離です。

**[HoverBorderColor](properties-color-border.md)** – コントロール上にユーザーがマウス ポインターを重ねているときのコントロールの境界線の色です。

**ItemColorSet** – グラフ内の各データ ポイントの色です。

**ItemsGap** – 縦棒グラフの縦棒間の距離です。

* **ItemsGap** プロパティは、**縦棒グラフ** コントロールでは使用できますが、**折れ線グラフ** コントロールでは使用できません。

**Markers** – 縦棒グラフまたは折れ線グラフで各データ ポイントの値を表示するかどうかを指定します。

**MarkerSuffix** – **Markers** プロパティが **true** に設定されている縦棒グラフで、各値の後に表示するテキストです。

* **MarkerSuffix** プロパティは、**縦棒グラフ** コントロールでは使用できますが、**折れ線グラフ** コントロールでは使用できません。

**MinimumBarWidth** – 縦棒グラフの縦棒の表示に可能な最も狭い幅です。

* **MinimumBarWidth** プロパティは、**縦棒グラフ** コントロールでは使用できますが、**折れ線グラフ** コントロールでは使用できません。

**[OnSelect](properties-core.md)** – ユーザーがコントロールをタップまたはクリックした場合のアプリの反応を指定します。

**[PaddingBottom](properties-size-location.md)** – コントロール内のテキストとそのコントロールの下端間の距離です。

**[PaddingLeft](properties-size-location.md)** – コントロール内のテキストとそのコントロールの左端間の距離です。

**[PaddingRight](properties-size-location.md)** – コントロール内のテキストとそのコントロールの右端間の距離です。

**[PaddingTop](properties-size-location.md)** – コントロール内のテキストとそのコントロールの上端間の距離です。

**[PressedBorderColor](properties-color-border.md)** – コントロールをユーザーがタップまたはクリックしたときのコントロールの境界線の色です。

**SeriesAxisMax** – 縦棒グラフまたは折れ線グラフの Y 軸の最大値です。

* **SeriesAxisMax** プロパティは、**縦棒グラフ** コントロールでは使用できますが、**折れ線グラフ** コントロールでは使用できません。

**SeriesAxisMin** – 縦棒グラフの Y 軸の最小値を決める値です。

* **SeriesAxisMin** プロパティは、**縦棒グラフ** コントロールでは使用できますが、**折れ線グラフ** コントロールでは使用できません。

**[Size](properties-text.md)** – コントロールに表示されるテキストのフォント サイズです。

**[Visible](properties-core.md)** – コントロールを表示するか非表示にするかを指定します。

**[Width](properties-size-location.md)** – コントロールの左端と右端の間の距離です。

**[X](properties-size-location.md)** – コントロールの左端とその親コンテナー (親コンテナーがない場合は画面) の左端間の距離です。

**XLabelAngle** – 縦棒グラフまたは折れ線グラフの X 軸の下に表示されるラベルの角度です。

**[Y](properties-size-location.md)** – コントロールの上端とその親コンテナー (親コンテナーがない場合は画面) の上端間の距離です。

**YAxisMax** – 折れ線グラフの Y 軸の最大値です。

* **YAxisMax** プロパティは、**縦棒グラフ** コントロールでは使用できますが、**折れ線グラフ** コントロールでは使用できません。

**YAxisMin** – 折れ線グラフの Y 軸の最小値です。

* **YAxisMin** プロパティは、**縦棒グラフ** コントロールでは使用できますが、**折れ線グラフ** コントロールでは使用できません。

**YLabelAngle** – 折れ線グラフまたは縦棒グラフの Y 軸の横に表示されるラベルの角度です。

## <a name="related-functions"></a>関連する関数
[**Max**( *DataSource*, *ColumnName* )](../functions/function-aggregates.md)

## <a name="example"></a>例
1. **[[ボタン]](control-button.md)** コントロールを追加し、**[OnSelect](properties-core.md)** プロパティに次の式を設定します。<br>
   **Collect(Revenue, {Year:"2013", Europa:24000, Ganymede:22300, Callisto:21200}, {Year:"2014", Europa:26500, Ganymede:25700, Callisto:24700},{Year:"2014", Europa:27900, Ganymede:28300, Callisto:25600})**
   
    [コントロールの追加および構成](../add-configure-controls.md)についてはこちらをご覧ください。
   
    **[Collect](../functions/function-clear-collect-clearcollect.md)** 関数または[その他の関数](../formula-reference.md)については各関連記事を参照してください。
2. F5 キーを押して、**[ボタン](control-button.md)** コントロールをクリックまたはタップしてから、Esc キーを押して既定のワークスペースに戻ります。
3. **縦棒グラフ** コントロールまたは**折れ線グラフ** コントロールを追加し、**[Items](properties-core.md)** プロパティを **Revenue** に、**NumberOfSeries** プロパティを **3** に設定します。
   
    コントロールに、過去 3 年間の各製品の売上データが表示されます。

