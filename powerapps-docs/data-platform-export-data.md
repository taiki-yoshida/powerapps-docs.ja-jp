---
title: "データのインポートとエクスポート | Microsoft Docs"
description: "エンティティをインポートまたはエクスポートします。"
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
ms.openlocfilehash: 880881b31362d38ed0d44126245dd96d2a74150f
ms.sourcegitcommit: 33099e6197c0139679cd08c42e9e2a5717904c92
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/12/2018
---
# <a name="import-or-export-data-from-the-common-data-service"></a>Common Data Service からのデータのインポートまたはエクスポート
Common Data Service との間でデータを移動する場合、次の 2 とおりの方法があります。

* 複数のエンティティのデータを一回限りで一括インポート/エクスポートしたい場合、Microsoft Excel を使用できます。
* 単一のエンティティのデータを別のサービス (Dynamics 365 や Salesforce など) や Excel ファイルとの間で日常的にインポート/エクスポートしたい場合、 [Microsoft Flow](https://flow.microsoft.com) を使用して日常的なインポート/エクスポートを設定することができます。

## <a name="import-or-export-data-once"></a>データの一回限りのインポートとエクスポート
### <a name="import-data-from-excel"></a>Excel からデータをインポートする
1. [powerapps.com](https://web.powerapps.com) で、**[Common Data Service]** セクションを展開し、左側のナビゲーション ウィンドウで **[エンティティ]** をクリックまたはタップします。
2. **[New entity (新しいエンティティ)]** の横の省略記号をクリックまたはタップし、**[Import data (データをインポート)]** をクリックまたはタップします。
3. データをインポートするエンティティを選択し、**[次へ]** をクリックまたはタップします。
4. **[検索]** をクリックまたはタップします。 インポートするデータがあるファイルを選択します。
5. **[Mapping Status]** (マッピングの状態) が**一致**せず、緑色のチェックマークが表示されない場合は、エンティティのフィールドと Excel ファイルの列との間でマッピングを指定する必要があります。 列をマッピングするには、次の手順を実行します。
   1. **[Show Mapping (マッピングを表示する)]** をクリックまたはタップします。
   2. 各エンティティ フィールドについて、Excel ファイル内の一致する列を選択します。
   3. **[Save changes (変更の保存)]** をクリックまたはタップします。
6. **[インポート]** をクリックします。

### <a name="export-data-to-excel"></a>Excel にデータをエクスポートする
標準エンティティまたはカスタム エンティティからデータを 1 回限りエクスポートしたり、複数のエンティティから一度にデータをエクスポートしたりすることができます。 複数のエンティティからデータをエクスポートした場合、各エンティティがそれぞれ異なる Microsoft Excel ファイルにエクスポートされます。

1. [powerapps.com](https://web.powerapps.com) の左側のナビゲーション ウィンドウで、**[エンティティ]** をクリックまたはタップします。
2. **[New entity (新しいエンティティ)]** の横の省略記号をクリックまたはタップし、**[データのエクスポート]** をクリックまたはタップします。
3. エクスポートするデータがあるエンティティを選択し、**[Excel にエクスポート]** をクリックまたはタップします。
4. "**エクスポートが完了しました**" と表示されたら、**[Download exported data (エクスポートされたデータのダウンロード)]** をクリックまたはタップして、データをダウンロードします。

## <a name="use-microsoft-flow-to-set-up-ongoing-import-or-export"></a>Microsoft Flow で日常的なインポート/エクスポートをセットアップする
日常的なインポート/エクスポートは、一度に 1 つの標準エンティティまたはカスタム エンティティに対して設定することができます。 接続先としては、次のような場所を選択することができます。

* Dynamics 365
* Salesforce
* 任意のクラウド ファイル プロバイダーに保存されている Microsoft Excel ファイル
* Microsoft SQL データベース (クラウドとオンプレミスの両方)
* 独自システムに接続するように定義されたカスタム コネクタ

現在、Microsoft Flow を使用してデータをインポートしたりエクスポートしたりする場合、その機能は完全な同期サービスではありません。 一方のサービスにオブジェクトを追加すると、そのオブジェクトがもう一方のシステムにもインポートされます。 しかしオブジェクトを一方のシステムから削除しても、そのオブジェクトがもう一方のシステムから削除されることはありません。

インポートの設定方法は、インポートしたいオブジェクトのテンプレートが既に存在するかどうかによって異なります。 テンプレートが存在する場合は、システム間でデータをコピーするための設定をテンプレートで行うことができます。 詳細については、「[Common Data Service を使用するフローの作成](https://flow.microsoft.com/documentation/common-data-model-intro/)」を参照してください。 ただし、そのようなテンプレートが存在しない場合は、データベースを使用できるフローを作成する必要があります。 詳細については、「[Microsoft Flow でのフローの作成](https://flow.microsoft.com/documentation/get-started-logic-flow/)」を参照してください。

