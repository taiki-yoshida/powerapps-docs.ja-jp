---
title: "カスタム エンティティの作成 | Microsoft Docs"
description: "カスタム エンティティで共通のデータ モデルを拡張します"
services: 
suite: powerapps
documentationcenter: na
author: mgblythe
manager: anneta
editor: 
tags: 
featuredvideoid: qg25q3MjFBo
courseduration: 6m
ms.service: powerapps
ms.devlang: na
ms.topic: get-started-article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 12/09/2016
ms.author: mblythe
ms.openlocfilehash: a28f64f1184e620430299ce4e8d32623172b3a08
ms.sourcegitcommit: 43be6a4e08849d522aabb6f767a81c092419babc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2017
---
# <a name="create-custom-entities"></a>カスタム エンティティの作成
Common Data Service は、小規模の店舗から大企業まで、すべてのビジネス カスタマー向けに設計されています。 共通のデータ モデルには、多くの一般的なビジネス シナリオに対応する一連の標準エンティティが含まれています。前のトピックでは、必要な場合に、これらの標準エンティティを拡張できることを学習しました。 しかし、ビジネスに固有の問題を解決するために、まったく異なるエンティティが必要になる場合があります。 そのような場合はカスタム エンティティが必要です。このトピックではカスタム エンティティを構築する方法を説明します。

エンティティを作成する方法は、2 つあります。

* 最初からエンティティを作成する。 このトピックではこの方法をとります。
* 別のエンティティのフィールドと設定をコピーして (そのデータはコピーしない)、そのエンティティをもとに新しいエンティティを作成する。

## <a name="creating-an-entity-from-scratch"></a>最初からエンティティを作成する
この例では、Product review (製品のレビュー) という名前のカスタム エンティティを最初から作成します。 まず、**[Entities]** (エンティティ) タブで **[New Entity]** (新しいエンティティ) をクリックします。 **エンティティ名** (スペースや特殊文字は含めない)、わかりやすい**表示名**、意味のある**説明**を入力します。 そして、**[Next]** (次へ) をクリックします。

![新しいエンティティ](./media/learning-common-data-service-custom-entities/new-entity.png)

次の画面には、既定のフィールドが 5 つ表示されています。これらはすべて標準エンティティとカスタム エンティティに含まれているものです。 **[Add field]** (フィールドの追加) をクリックして、独自のフィールドの追加を開始します。

![既定のエンティティ フィールド](./media/learning-common-data-service-custom-entities/default-fields.png)

この例では、次の 4 つのフィールドを追加しましょう。

* **Review Date** (レビュー日)。日付フィールド、必須。
* **Product Rating** (製品評価)。整数フィールド、必須。 ここでは、特定の値 (1 ～ 5 など) だけを指定できる候補リストを使うこともできますが、いったん使用しないでわかりやすくしておきます。
* **Reviewer Name** (レビュー担当者名)。テキスト フィールド。必須ではありません。
* **Reviewer Comment** (レビュー担当者コメント)。テキスト フィールド。このフィールドも必須ではありません。 

エンティティに満足したら、**[Create]** (作成) をクリックします。 エンティティは、作成されたときはデータがありません。 データをインポートする方法は、次のトピックで説明します。

![カスタム エンティティ フィールド](./media/learning-common-data-service-custom-entities/custom-fields.png)

## <a name="creating-a-relationship-between-two-entities"></a>2 つのエンティティ間のリレーションシップを作成する
各レビューを特定の製品に関連付けたいので、Product review (製品のレビュー) エンティティと Product (製品) エンティティの間のリレーションシップを作成する必要があります。 Product review (製品のレビュー) エンティティの **[Relationships]** (リレーションシップ) タブで **[New relationship]** (新しいリレーションシップ) をクリックします。 次に、**[Related entity]** (関連エンティティ) を選択して、**名前**、**表示名**、および**説明**を入力します。 **[Save]** (保存) をクリックしてリレーションシップを作成します。

![エンティティ間のリレーションシップを作成する](./media/learning-common-data-service-custom-entities/create-entity-relationship.png)

## <a name="connecting-to-a-custom-entity-in-powerapps-studio"></a>PowerApps Studio でカスタム エンティティに接続する
PowerApps Studio でカスタム エンティティに接続する方法は、標準エンティティの接続とほとんど同じです。 **[New]** (新規) をクリックして、**[Common Data Service]** の下の **[Phone layout]** (電話レイアウト) をクリックします。 左側に使用できるデータ接続、右側にエンティティのリストが表示されます。

![PowerApps Studio でエンティティに接続する](./media/learning-common-data-service-custom-entities/connect-to-custom-entity.png)

次のトピックでは、Common Data Service でデータを管理する方法を説明します。

