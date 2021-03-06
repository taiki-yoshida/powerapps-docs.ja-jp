---
title: 'Power BI タイル コントロール: リファレンス | Microsoft Docs'
description: 各種プロパティとサンプルを含む Power BI のタイル コントロールに関する情報です
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
ms.date: 07/07/2016
ms.author: fikaradz
ms.openlocfilehash: 1f351877e3c05b83b4bd9cfa104a7eb22cef5028
ms.sourcegitcommit: 59785e9e82da8f5bd459dcb5da3d5c18064b0899
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/22/2018
---
# <a name="power-bi-tile-control-in-powerapps"></a>PowerApps の Power BI タイル コントロール
アプリ内の [Power BI](https://powerbi.microsoft.com) タイルを表示するコントロール。

## <a name="description"></a>説明
アプリ内の **[Power BI タイル](https://docs.microsoft.com/power-bi/service-dashboard-tiles)**を表示して、既存のデータ分析とレポートを活用します。  オプション パネルの **[データ]** タブで **Workspace**、**Dashboard** および **Tile** プロパティを設定して、表示するタイルを選択します。

## <a name="sharing-and-security"></a>共有とセキュリティ
一度共有すると、アプリのアクセス権を持つすべてのユーザーが PowerApp にアクセスできます。  ただし、Power BI のコンテンツをそれらのユーザーに表示されるようにするのには、タイルの情報源であるダッシュボードを、Power BI のユーザーに[共有](https://docs.microsoft.com/power-bi/service-how-to-collaborate-distribute-dashboards-reports)する必要があります。  これによって、アプリ上で Power BI のコンテンツにアクセスする場合に、Power BI の共有アクセス許可が適切に扱われるようになります。

## <a name="key-properties"></a>主要なプロパティ
**ワークスペース** – タイルの情報源である Power BI ワークスペース。

**ダッシュボード** – タイルの情報源である Power BI のダッシュボード。

**タイル** – 表示する Power BI のタイルの名前。

## <a name="additional-properties"></a>その他のプロパティ
**[BorderColor](properties-color-border.md)** – コントロールの境界線の色です。

**[BorderStyle](properties-color-border.md)** – コントロールの境界線を **Solid** (実線)、**Dashed** (破線)、**Dotted** (点線)、**None** (なし) のいずれに指定します。

**[BorderThickness](properties-color-border.md)** – コントロールの境界線の太さです。

**[DisplayMode](properties-core.md)** – コントロールで、ユーザー入力を許可するか (**Edit**)、データの表示のみを許可するか (**View**)、許可しないか (**Disabled**) を設定します。

**[Height](properties-size-location.md)** – コントロールの上端と下端の距離です。

**[OnSelect](properties-core.md)** – ユーザーがコントロールをタップまたはクリックした場合のアプリの反応を指定します。 既定の動作では、ユーザーはタイルに関連付けられた Power BI レポートに移動します。

**[Visible](properties-core.md)** – コントロールを表示するか非表示にするかを指定します。

**[Width](properties-size-location.md)** – コントロールの左端と右端の間の距離です。

**[X](properties-size-location.md)** – コントロールの左端とその親コンテナー (親コンテナーがない場合は画面) の左端間の距離です。

**[Y](properties-size-location.md)** – コントロールの上端とその親コンテナー (親コンテナーがない場合は画面) の上端間の距離です。

## <a name="example"></a>例
1. **[コントロール]** メニューの **[挿入]** タブから **[Power BI タイル]** コントロールを追加します。  
2. オプション パネルの **[データ]** タブで、**[ワークスペース]** 設定に、"[マイ ワークスペース]" を選択します。  ダッシュボードの一覧からダッシュボードを 1 つ選択し、タイルの一覧からタイルを 1 つ選択します。
   
    コントロールが Power BI タイルを表示します。
   
    [コントロールの追加および構成](../add-configure-controls.md)についてはこちらをご覧ください。
   
   Power BI をお持ちではありませんか。 [サインアップ](https://docs.microsoft.com/power-bi/service-self-service-signup-for-power-bi)してください。

