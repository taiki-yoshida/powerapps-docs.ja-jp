---
title: "アプリの生成 (Common Data Service) | Microsoft Docs"
description: "Common Data Service から 3 画面アプリを作成します"
services: 
suite: powerapps
documentationcenter: na
author: mgblythe
manager: anneta
editor: 
tags: 
featuredvideoid: Gi5TQF7_pz8
courseduration: 6m
ms.service: powerapps
ms.devlang: na
ms.topic: get-started-article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 12/09/2016
ms.author: mblythe
ms.openlocfilehash: 64e34da9afcecde950094ff40808c99176bccc13
ms.sourcegitcommit: 43be6a4e08849d522aabb6f767a81c092419babc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2017
---
# <a name="generate-an-app-common-data-service"></a>アプリの生成 (Common Data Service)
コースのこのセクションでは、Common Data Service の*エンティティ*をベースにアプリを作成します。 エンティティは共有データのチャンクで、変更、保存、取得、および対話することができます。 エンティティからアプリを生成して、アプリをカスタマイズする方法、別のデータ ソースを追加する方法、アプリからフローを呼び出す方法を説明します。 SharePoint リストからのアプリ作成に関するセクションを学習済みの場合は、同じ領域について説明することになりますが、特にアプリのカスタマイズについてより詳しく説明します。

組織全体のハードウェアおよびソフトウェアに関する問題の追跡、優先順位付け、および処理に IT 部門が使用できるようなケース管理アプリを作成します。 トピックを読み進めると、このようなアプリの他の用途も思い浮かぶかもしれません。 アプリ データの保存によく適しているため Common Data Service のデータを使用していますが、別のデータ ソースを使用して同じアプリを構築することもできます。

PowerApps には、これから構築するアプリと同じエンティティを使用する、より複雑なケース管理テンプレートが含まれています。 このセクションを完了したら、このテンプレートを詳しく確認して、PowerApps で何が構築できるのかを把握することをお勧めします。

## <a name="create-a-common-data-service-database"></a>Common Data Service データベースの作成
まだ Common Service データベースを作成していない場合は、このアプリを構築する最初の手順で作成します。 Common Data Service データベースは*環境*内に作成します。 環境は、アプリおよびその他のリソースのコンテナーです (環境についてはコースの後半で詳しく学習します)。 *環境管理者*が次の手順でデータベースを作成してください (管理者以外のユーザーは組織の管理者に問い合わせてください)。

**[Home]** (ホーム) タブから、**[Create Database]** (データベースの作成) をクリックします。

![Common Data Service データベースの作成](./media/learning-case-app-generate/create-database.png)

データベースへのアクセスを制限するかどうかを指定し (データベースは開いたままにします)、**[Create my database]** (データベースを作成) をクリックします。

![Common Data Service アクセス権の指定](./media/learning-case-app-generate/specify-access.png)

プロセスが完了したら、共通のデータ モデルに含まれている標準的なエンティティがすべて表示されます。 以下にその一部を示します。

![Common Data Service の標準エンティティ](./media/learning-case-app-generate/standard-entities.png)

## <a name="generate-an-app-from-the-case-entity"></a>Case (ケース) エンティティからアプリを生成する
データベースが作成されたところで、Case (ケース) エンティティに接続し、アプリを生成します。 **[New app]** (新しいアプリ) をクリックして、**[PowerApps Studio for web]** をクリックします。

![[PowerApps Studio for web] の [New app] (新しいアプリ)](./media/learning-case-app-generate/choose-studio.png)

Common Data Service エンティティの電話アプリを構築するので、**[Common Data Service]** の下の **[Phone layout]** (電話レイアウト) をクリックまたはタップします。

![[Common Data Service] の [Phone app] (電話アプリ)](./media/learning-case-app-generate/common-phone.png)

次の画面で、接続と接続先のエンティティを選択して、**[Connect]** (接続) をクリックします。

![Case (ケース) エンティティへの [接続]](./media/learning-case-app-generate/connect-entity.png)

**[Connect]** (接続) をクリックすると、PowerApps がアプリの生成を開始します。 PowerApps は、データに関するあらゆる推論を行うため、開始点として便利なアプリが生成されます。

## <a name="view-the-app-in-powerapps-studio"></a>PowerApps Studio でアプリを表示する
新しい 3 画面アプリが PowerApps Studio で開きます。 データから生成されたすべてのアプリには、同じ画面セットが含まれています。

* **ブラウズ**画面: リストから取得したデータを参照、並べ替え、フィルター処理、更新し、(+) アイコンをクリックして項目を追加する画面。
* **詳細**画面: 項目の詳細を表示し、項目の削除または編集ができる画面。
* **編集/作成**画面: 既存の項目を編集したり、新規に作成する画面。

左側のナビゲーション バーで、右上のアイコンをクリックまたはタップしてサムネイル表示に切り替えます。

![表示の切り替え](./media/learning-case-app-generate/toggle-view.png)

各サムネイルをクリックまたはタップすると、その画面上のコントロールが表示されます。

![生成されたアプリ](./media/learning-case-app-generate/finished-app.png)

次は、アプリをさらに詳しく確認した後で、ニーズに合うようにアプリをカスタマイズします。

