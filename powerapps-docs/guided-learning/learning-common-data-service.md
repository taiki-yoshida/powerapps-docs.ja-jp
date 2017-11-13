---
title: Common Data Service | Microsoft Docs
description: "データを保存してモデル化する強力な方法を理解する"
services: 
suite: powerapps
documentationcenter: na
author: mgblythe
manager: anneta
editor: 
tags: 
featuredvideoid: os33pHQ9jSU
courseduration: 5m
ms.service: powerapps
ms.devlang: na
ms.topic: get-started-article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 12/09/2016
ms.author: mblythe
ms.openlocfilehash: 37385bb20f15296e3002f3258cae437220a63910
ms.sourcegitcommit: 43be6a4e08849d522aabb6f767a81c092419babc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2017
---
# <a name="the-common-data-service"></a>Common Data Service
データは、ビジネス アプリケーションとビジネス プロセスの中核です。これには Excel、SQL Server のようなオンプレミス ソース、および Salesforce や SharePoint Online などのクラウド ソースからのデータがあります。 データは、顧客、販売、従業員などの多くのことに関連しているものですが、共通しているのは、データがビジネスにとって不可欠であり、PowerApps でビルドするアプリで重要な役割を果たすということです。 このコースではこれまで、複数の種類のデータ ソースについて学び、使用してきました。また、Microsoft Common Data Service についても以前に紹介しました。 このセクションでは、その詳細とメリットを説明し、サービスの使用方法を紹介します。

## <a name="understanding-the-service"></a>サービスについて
下に図が 2 つあります。 1 つ目の図は以前ご覧になったことがあるかもしれません。Microsoft ビジネス アプリケーション プラットフォームのコンポーネントを表したものです。 現時点で既に PowerApps についてはよくご存じでしょうし、Microsoft Flow、Power BI やその他のコンポーネントも使用したことがあるかもしれません。 ここでわかることは、Common Data Service およびコネクタとゲートウェイがこれらすべてのコンポーネントに関連しているということです。 現時点では、Common Data Service は主に PowerApps と Microsoft Flow で使用されていますが、いずれはその他のコンポーネントでも利用可能になります。

![ビジネス プラットフォームの図](./media/learning-common-data-service/business-platform.png)

Common Data Service の位置付けがわかったところで、次はその中の部分を見てみましょう。 Common Data Service は階層として捉えてください。 最下位レベルでは、スケーラブルで信頼性の高い方法でデータが格納され、複数のアプリケーションでデータを利用できます。 次のレベルは、アプリケーションとビジネス プロセスで使用される、多くのエンティティを含む共通のデータ モデルです。エンティティには、アカウント、連絡先、製品、および販売注文などがあります。 標準のエンティティを拡張して、ビジネス ニーズを満たす独自のエンティティを作成できます。

![Common Data Service のアーキテクチャ図](./media/learning-common-data-service/architecture.png)

エンティティとは単に、エンティティを記述するメタデータ (フィールド名やデータの型など) と、そこに保存するデータの組み合わせを指します。 Access などのデータベースをご存じでしょうか。エンティティはテーブルに非常によく似ています。 エンティティの詳細については次のトピックで触れますが、ここでは Common Data Service でエンティティ データを利用することのメリットについて考えます。

* **管理が容易**: メタデータとデータはどちらもクラウド上に保存されます。 保存方法の詳細を気にする必要がありません。
* **共有が容易**: アクセス許可は PowerApps が管理するため、同僚とのデータの共有が容易になります。
* **セキュリティ保護が容易**: データが安全に保存されるため、アクセスが許可されたユーザー以外はデータを表示できません。 ロール ベースのセキュリティにより、組織内のユーザー別にエンティティへのアクセスを制御できます。
* **豊富なメタデータ**: データの型とリレーションシップは PowerApps 内で直接活用されます。 たとえば、フィールド タイプ URL を定義すると、アプリ内でデータがハイパーリンクとして表示されます。
* **生産性向上ツール**: エンティティは、Microsoft Excel および Outlook 内のアドイン内で利用可能で、生産性を向上させ、データを常にアクセス可能にします。
* **候補リスト**: 豊富な標準ピックリストのセットを含み、エンティティとアプリ内ですばやくドロップ ダウンを提供します。

## <a name="create-a-common-data-service-database"></a>Common Data Service データベースの作成
Common Data Service データベースは*環境*内に作成します。 環境については以前このコースで説明したため、簡単に復習すると、環境とは、Common Data Service のようなアプリやその他のリソースのコンテナーを指します。 各環境にはサービスのインスタンスを 1 つだけ関連付けることができます。 環境の管理者で、サービスを環境に追加する場合は、以下の手順を実行します。

**[Home]** (ホーム) タブから、**[Create Database]** (データベースの作成) をクリックします。

![Common Data Service データベースの作成](./media/learning-common-data-service/create-database.png)

データベースへのアクセスを制限するかどうかを指定し、**[Create my database (データベースを作成)]** をクリックします。

![Common Data Service アクセス権の指定](./media/learning-common-data-service/specify-access.png)

プロセスが完了したら、共通のデータ モデルに含まれている標準的なエンティティがすべて表示されます。 以下にその一部を示します。

![Common Data Service の標準エンティティ](./media/learning-common-data-service/standard-entities.png)

これまでにデータベースを使用したことがない場合は、今回のトピックにはなじみのない箇所があったかもしれません。 しかし全般的な概念はきわめて簡単で、Common Data Service により、安全かつ信頼性の高い方法でデータを保存し、アカウント、連絡先、製品、および販売注文のような一般的なエンティティの観点からデータを扱うことができます。 次のトピックでは、エンティティの詳細を説明します。

