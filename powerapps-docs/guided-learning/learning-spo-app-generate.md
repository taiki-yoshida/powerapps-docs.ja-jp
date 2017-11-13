---
title: "アプリの生成 (SharePoint リスト) | Microsoft Docs"
description: "SharePoint リストから 3 画面アプリを生成します"
services: 
suite: powerapps
documentationcenter: na
author: mgblythe
manager: anneta
editor: 
tags: 
featuredvideoid: m6KfAwEdtYU
courseduration: 3m
ms.service: powerapps
ms.devlang: na
ms.topic: get-started-article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 12/09/2016
ms.author: mblythe
ms.openlocfilehash: a6ae0ec73d659563275be5670c4aeda9dc3e172a
ms.sourcegitcommit: 43be6a4e08849d522aabb6f767a81c092419babc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2017
---
# <a name="generate-an-app-sharepoint-list"></a>アプリの生成 (SharePoint リスト)
コースのこのセクションでは、SharePoint リストの Flooring Estimates (床材見積もり) からアプリを作成します。 作成するアプリは、リストを参照したりリストを最新に保ったりするために、客先にいる見積もり担当者などが使用することが考えられます。 概要のセクションで、同じリストからアプリを生成する方法を説明しました。それでは、なぜもう一度確認するのでしょうか。 まずは、PowerApps Studio で開始せずに、PowerApps がどのように SharePoint Online に統合されているかを説明します。 次に、アプリの構造をさらに掘り下げ、カスタマイズする方法を説明します。 このセクションを読み進めれば新しい情報を手に入れることができます。では、はじめましょう。

## <a name="generate-the-app"></a>アプリを生成する
下図に、SharePoint リストの Flooring Estimates (床材見積もり) を示します。このリストには、名前、価格、各床材タイプの画像などの基本情報が含まれています。 PowerApps と Microsoft Flow がどのように SharePoint Online に統合されているか確認することができるので、リストから簡単にアプリとフローを構築できます。

![Flooring Estimates (床材見積もり) リスト](./media/learning-spo-app-generate/flooring-estimates-list.png)

アプリを構築するには、**[PowerApps]** > **[Create an app]** (アプリの作成) の順にクリックします。 右側のウィンドウで、アプリの名前を入力して、**[Create]** (作成) をクリックします。 **[Create]** (作成) をクリックすると、PowerApps がアプリの生成を開始します。 PowerApps は、データに関するあらゆる推論を行うため、開始点として便利なアプリが生成されます。

![リストからアプリを生成する](./media/learning-spo-app-generate/generate-app.png)

## <a name="view-the-app-in-powerapps-studio"></a>PowerApps Studio でアプリを表示する
新しい 3 画面アプリが PowerApps Studio で開きます。 データから生成されたすべてのアプリには、同じ画面セットが含まれています。

* **ブラウズ**画面: リストから取得したデータを参照、並べ替え、フィルター処理、更新し、(+) アイコンをクリックして項目を追加する画面。
* **詳細**画面: 項目の詳細を表示し、項目の削除または編集ができる画面。
* **編集/作成**画面: 既存の項目を編集したり、新規に作成する画面。

左側のナビゲーション バーで、右上のアイコンをクリックまたはタップしてサムネイル表示に切り替えます。

![表示の切り替え](./media/learning-spo-app-generate/toggle-view.png)

各サムネイルをクリックまたはタップすると、その画面上のコントロールが表示されます。

![生成されたアプリ](./media/learning-spo-app-generate/generate-finished-app.png)

## <a name="run-the-app-in-preview-mode"></a>アプリをプレビュー モードで実行する
右上にある ![アプリのプレビューを開始する矢印を](./media/learning-spo-app-generate/f5-arrow-sm.png) クリックまたはタップしてアプリを実行します。 アプリ全体を見ると、アプリにリストのすべてのデータが含まれていて、アプリが既定で良いエクスペリエンスを提供していることが分かります。

![アプリをプレビュー モードで実行する](./media/learning-spo-app-generate/generate-run-app.png)

次は、アプリをさらに詳しく確認した後で、ニーズに合うようにアプリをカスタマイズします。

