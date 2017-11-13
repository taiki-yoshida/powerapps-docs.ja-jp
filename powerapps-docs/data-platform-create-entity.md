---
title: "カスタム エンティティの作成 | Microsoft Docs"
description: "カスタム エンティティを別のエンティティから、または最初から作成します。"
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
ms.openlocfilehash: 5d927e84144da8e3b011bb4e4a7ac107aedac74f
ms.sourcegitcommit: 43be6a4e08849d522aabb6f767a81c092419babc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2017
---
# <a name="create-a-custom-entity"></a>カスタム エンティティの作成
組織に固有のデータを格納するカスタム エンティティを作成することができます。 エンティティを参照するアプリを開発すると、そのデータを表示できるようになります。

エンティティを作成する方法は、2 つあります。

* 最初からエンティティを作成する。 既定では、エンティティには [4 つのシステム フィールドと 1 つのレコード タイトル フィールド](data-platform-create-entity.md#system-and-record-title-fields)のみが格納されます。
* 別のエンティティのフィールドと設定をコピーして (そのデータはコピーしない)、そのエンティティをもとに新しいエンティティを作成する。

どちらのケースも、Microsoft PowerApps によって自動的にデータが保存され、セキュリティが確保されます。 エンティティの作成後、[そのフィールドを作成または編集](data-platform-manage-fields.md)したり、[エンティティ間のリレーションシップを構築](data-platform-entity-lookup.md)したりすることができます。

**注:** エンティティを作成する前に、[標準エンティティの一覧](data-platform-intro.md#standard-entities)を参照してください。 これらのエンティティには、アカウントや連絡先などの一般的なシナリオが含まれています。 これらのエンティティのいずれかが既に要件を満たしているか、わずかな変更のみで要件を満たす場合は、そのエンティティを使用することで時間を節約することができます。

## <a name="create-an-entity"></a>エンティティの作成
1. 1. [powerapps.com](https://web.powerapps.com) で、**[Common Data Service]** セクションを展開し、左側のナビゲーション ウィンドウで **[エンティティ]** をクリックまたはタップします。
2. データベースを作成していない場合は、作成する必要があります。 詳細については、「[Create a Common Data Service database (Common Data Service サービスの作成)](create-database.md)」を参照してください。
3. 右上隅にある **[新しいエンティティ]** をクリックまたはタップします。
4. **[エンティティ名]** フィールドに、エンティティの名前を入力します。 明確でわかりやすいエンティティ名を指定してください。この名前はエンティティの作成後に変更することはできません。 この名前は、アプリを開発するときに式の中でエンティティを参照する際に使用します。
5. エンティティの表示名と、必要に応じて説明を入力し、**[次へ]** をクリックまたはタップします。
6. 省略可: **Title** フィールドの値を、実際のデータの内容に合った名前に変更します。
7. **[作成]** をクリックまたはタップしてエンティティを作成します。

作成したエンティティが、データベース内のエンティティの一覧に表示されます。 エンティティを一覧の先頭に表示するには、**[種類]** という列ヘッダーをクリックまたはタップします。 エンティティが種類別に並べ替えられ、すべてのカスタム エンティティが標準エンティティよりも上に表示されます。

## <a name="system-fields-and-the-record-title-field"></a>システム フィールドとレコード タイトル フィールド
すべてのエンティティには、システム フィールドが 5 つ存在します。 これらのフィールドは、読み取り専用です。 そのため、変更したり削除したりすることはできません。値を割り当てることもできません。

| 表示名 | システム フィールド名 | データ型 | 説明 |
| --- | --- | --- | --- |
| Id |システム フィールド名 |Big Integer |レコードの一意の識別子。 |
| Created By |CreatedByUser |テキスト |レコードを作成したユーザー。 |
| Created Record Date |CreatedOnDateTime |DateTime |レコードが作成された日時。 |
| Last modified By |LastModifiedByUser |テキスト |前回レコードを変更したユーザー。 |
| Modified Record Date |LastModifiedDateTime |DateTime |前回レコードが変更された日時。 |

最初から作成したエンティティには、**Title** という名前のカスタム フィールドも含まれています。 このフィールドは、レコードの **Title** フィールドとして設定されています。 **Title** フィールドの値は、アプリ内で使用するレコードを常にわかりやすく示す識別子です。 どのフィールドを **Title** フィールドにするかは変更できますが、**Title** フィールドは、すべてのエンティティに必ず 1 つ存在する必要があります。

## <a name="next-steps"></a>次の手順
* [エンティティのフィールドを管理する](data-platform-manage-fields.md)
* [エンティティ間のリレーションシップを定義する](data-platform-entity-lookup.md)
* [Common Data Service データベースを使用してアプリを生成する](data-platform-create-app.md)
* [Common Data Service データベースを使用してアプリを最初から作成する](data-platform-create-app-scratch.md)

## <a name="privacy-notice"></a>プライバシーに関する声明
Microsoft PowerApps の Common Data Service では、Microsoft の診断システムにカスタム エンティティとフィールド名を収集して格納します。  収集した情報は、お客様向けの Common Data Service の改善に使用します。 作成者が作成するエンティティとフィールド名は、Microsoft PowerApps コミュニティ全体で共通するシナリオを理解したり、組織に関するスキーマなどの、サービスの標準エンティティの対象範囲のギャップを確認したりする場合に役立ちます。 このエンティティに関連するデータベース テーブルのデータに、Microsoft がアクセスまたは使用することはありません。また、データベースがプロビジョニングされているリージョン外にデータがレプリケートされることもありません。 ただし、カスタム エンティティとフィールド名はリージョン間でレプリケートされ、Microsoft のデータ保持ポリシーに基づいて削除される場合があります。 Microsoft はお客様のプライバシーを尊重いたします。詳細については、[Trust Center](https://www.microsoft.com/trustcenter/Privacy/default.aspx) を参照してください。

