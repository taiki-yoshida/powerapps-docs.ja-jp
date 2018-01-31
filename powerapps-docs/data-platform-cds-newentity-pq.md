---
title: "Power Query を使用して Common Data Service (CDS) で新しいエンティティを作成する | Microsoft Docs"
description: "Power Query を使用して CDS で新しいエンティティを作成するための詳しい手順。"
services: 
suite: powerapps
documentationcenter: na
author: mllopis
manager: kfend
editor: 
tags: 
ms.service: powerapps
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 08/18/2017
ms.author: millopis
ms.openlocfilehash: 18f580c06412968b27a279a526b562e27cb89e26
ms.sourcegitcommit: 6afca7cb4234d3a60111c5950e7855106ff97e56
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2018
---
# <a name="create-new-entities-in-the-common-data-service-cds-using-power-query"></a>Power Query を使用して Common Data Service (CDS) で新しいエンティティを作成する
**Power Query** の統合を使用すると、ビジネス アプリ開発者は Common Data Service (CDS) で幅広いデータソースから新しいエンティティを作成できます。

ユーザーは **Common Data Service** を使用すると、一連の標準エンティティとカスタム エンティティ内にデータを安全に格納して、管理できます。 *エンティティ*は、データベース内のテーブルと同様に、データを格納するために使用される一連のフィールドです。 Common Data Service にデータが格納されたら、**Microsoft PowerApps** で、格納されたデータを使用するさまざまなアプリケーションを構築できます。

**Power Query** の統合を使用すると、PowerApps を使用するビジネス アプリ開発者は、**Common Data Service** にリレーショナル データベース ( SQL Server、IBM DB2 など)、Excel、Access、テキスト ファイルに加えて、Salesforce、Azure SQL Database およびデータ ウェアハウス、Web API、OData フィード、その他のソースのオンライン サービスのようなオンプレミス データ ソースなどの外部データ ソースのデータに基づき、新しいエンティティを作成できます。 **Power Query** を使用すると、さまざまなデータ ソースに接続できる上に、Common Data Service にデータを読み込む前にフィルター処理、変換、データの結合もできます。

![データからの新しいエンティティ](media/data-platform-cds-newentity-pq/data-platform-cds-pq-01.jpg)

## <a name="enabling-the-cds-new-entities-from-power-query-feature"></a>Power Query の機能を使用して CDS の新しいエンティティを有効にする
この機能は PowerApps テナントで利用できますが、既定ではオンになっていません。 [web.powerapps.com](https://aka.ms/pqocds) で有効にすることができます。

> [!NOTE]
> 自分で作成したデータベースでのみ、新しいカスタム エンティティを作成できます。

この機能を有効にするには、PowerApps ポータルで次の手順を実行します。

1. 左側のナビゲーション ウィンドウで、**[Common Data Service] > [エンティティ]** タブを参照します。

2. **エンティティ**一覧から、**[新しいエンティティ]** のドロップダウンを選択します。

3. ドロップダウン メニューに表示される一覧から、次の図のように **[データからの新しいエンティティ (Technical Preview)]** を選択します。
   
    ![データからの新しいエンティティ](media/data-platform-cds-newentity-pq/data-platform-cds-pq-02.jpg)
4. メニューで **[データからの新しいエンティティ (Technical Preview)]** を選択すると、次の図のように、ダイアログとともにこの Technical Preview で使用可能なコネクタの一覧が表示されます。
   
   ![使用可能なコネクタ](media/data-platform-cds-newentity-pq/data-platform-cds-pq-03.jpg)
5. 使用するコネクタを選択したら、次の手順に進み、データ ソース接続の詳細と資格情報を指定したり、インポートするテーブルを選択したりします。 **クエリ エディター**にもアクセスできるようになるため (**[ナビゲーター]** ビューの **[編集]** ボタンを使用します)、CDS にデータをインポートする前に、フィルター処理やデータ変換の手順を適用できます。
   
    ![](media/data-platform-cds-newentity-pq/data-platform-cds-pq-04.jpg)

## <a name="adjust-load-settings-and-other-behavior"></a>読み込みの設定とその他の動作を調整する
前のセクションの手順が完了し、**Power Query** を使用して新しいエンティティを CDS に作成するためのデータ ソースの準備が整ったら、更新動作などのその他の読み込みの設定、表示名や主キーなどのエンティティ特有の設定を調整できます。

![](media/data-platform-cds-newentity-pq/data-platform-cds-pq-05.jpg)

上記の手順を完了して **[読み込み]** を選択すると、CDS に新しいカスタム エンティティが作成されます。 特定のエンティティの**[エンティティ]** メニューにアクセスして、初期読み込みの後にクエリを編集することもできます。

これはとても心躍る機能です。お客様のご意見をお待ちしております。 この機能に関する[提案およびフィードバックをお寄せください](https://powerusers.microsoft.com/t5/PowerApps-Community/ct-p/PowerApps1)。

