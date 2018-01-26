---
title: "Common Data Service データベースを使用してアプリを最初から作成する | Microsoft Docs"
description: "レコードを追加、更新、および削除するアプリを作成します。"
services: powerapps
documentationcenter: na
author: kfend
manager: kfend
editor: 
tags: 
ms.service: powerapps
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 12/06/2016
ms.author: kfend
ms.openlocfilehash: 214b11c4f23db29d097b2d97052473d8f436d533
ms.sourcegitcommit: 6afca7cb4234d3a60111c5950e7855106ff97e56
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2018
---
# <a name="create-an-app-from-scratch-using-a-common-data-service-database"></a>Common Data Service データベースを使用してアプリを最初から作成する
Common Data Service に保存されているデータを、標準エンティティ (組み込み)、カスタム エンティティ (組織が作成)、またはその両方を使用して管理するアプリを構築します。

Common Data Service からアプリを構築する場合、SharePoint、Dynamics 365、Salesforce などのデータ ソースが利用できるので、Microsoft PowerApps から接続を作成する必要はありません。 アプリの両方のアクティビティで表示、管理、または使用するエンティティの指定のみが必要です。




1. Common Data Service データベースを作成します。 詳細については、「[Create a Common Data Service database (Common Data Service サービスの作成)](create-database.md)」を参照してください。
2. [powerapps.com](https://web.powerapps.com) の左側のナビゲーション ウィンドウで、**[新しいアプリ]** をクリックまたはタップします。
3. 表示されたダイアログ ボックスで、**[Web 用の PowerApps Studio]** をクリックまたはタップします。 (**[PowerApps Studio for Windows]** をクリックまたはタップして、指示に従って PowerApps Studio for Windows をインストールすることもできます。 以後の手順では Web 用の PowerApps Studio を使用しますが、Microsoft Windows 用アプリの手順も似ています。)
4. **[Start with a blank canvas or template]** (空のキャンバスまたはテンプレートから開始する) の下の **[空のアプリ]** タイルで **[携帯電話レイアウト]** をクリックまたはタップします。
5. メッセージが表示されたら、**[スキップ]** をクリックまたはタップすると、チュートリアルがスキップします。
6. **[コンテンツ]** タブをクリックまたはタップします。
7. **[データ ソース]** をクリックまたはタップします。
8. 一番右側のウィンドウで **[データ ソースの追加]** をクリックまたはタップします。
9. 使用する Common Data Service をクリックまたはタップします。
10. エンティティの一覧で、使用する 1 つ以上のエンティティのチェック ボックスを選択し、**[接続]** をクリックまたはタップします。

指定したエンティティがデータ ソースの一覧に表示され、「[アプリをゼロから作成](get-started-create-from-blank.md)」に記載されているとおりにアプリを構築できます。

