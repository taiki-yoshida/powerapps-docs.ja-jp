---
title: "Common Data Service データベースの作成 | Microsoft Docs"
description: "Common Data Service データベースを作成します。"
services: powerapps
documentationcenter: na
author: nimakms
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
ms.openlocfilehash: a2224d97c9cfc1261e43f7d30c8d8bdd2dd6e86b
ms.sourcegitcommit: 33099e6197c0139679cd08c42e9e2a5717904c92
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/12/2018
---
# <a name="create-a-common-data-service-database"></a>Common Data Service データベースの作成
データベースの作成とアプリの構築には、Common Data Service をデータ ストアとして使用できます。 独自のカスタム エンティティを作成することも、事前定義されたエンティティを使用することもできます。 データベースを作成するには、まず環境を作成するか、管理者として既存の環境に割り当てられる必要があります。 さらに、適切なライセンスが割り当てられている必要があります。 Common Data Service を使用するためのプランの購入については、[価格情報](pricing-billing-skus.md)に関するページを参照してください。

データベースを作成する方法は 3 つあります。

* 管理センターで作成する
* powerapps.com の **[ホーム]** ウィンドウで作成する
* powerapps.com の **[エンティティ]** ウィンドウで作成する

## <a name="create-a-database-in-the-admin-center"></a>管理センターでのデータベースの作成
1. [管理センター](https://admin.powerapps.com)で、左側のナビゲーション ウィンドウの **[環境]** をクリックします。
2. 環境を選択するか、必要に応じて新しい環境を作成します。
3. **[データベース]** タブの **[データベースの作成]** をクリックします。 既定では、作成されるデータベースのアクセス モードはオープンになっています。
4. セキュリティを適用する場合は、**[Restrict access (アクセスを制限する)]** を選択します。

## <a name="create-a-database-in-the-home-pane-of-powerappscom"></a>powerapps.com の [ホーム] ウィンドウでのデータベースの作成
1. [powerapps.com](https://web.powerapps.com) の左側のナビゲーション ウィンドウで、**[ホーム]** をクリックします。
2. **[Microsoft Common Data Service を使う]** セクションで、**[Create database (データベースの作成)]** または **[Get started (開始する)]** という名前のボタンを探します。 このボタンの名前は、割り当てられているライセンスとアクセス許可に応じて異なります。 現在の環境でデータベースの作成が許可されていない場合もあります。

### <a name="create-database-in-current-environnmet"></a>現在の環境でデータベースを作成する
1. **[Create database (データベースの作成)]** をクリックします。
2. セキュリティを適用したい場合、ダイアログ ボックスで **[Restrict access to database (データベースへのアクセスを制限する)]** チェック ボックスをオンにします。
3. **[自分のデータベースを作成]** をクリックします。

### <a name="get-started-by-creating-a-new-environment"></a>新しい環境を作成して開始する
1. **[Get started (開始する)]** をクリックします。
2. ダイアログ ボックスで **[新しい環境を作成する]** をクリックし、新しい環境とデータベースの作成を開始します。
3. **[環境名]** フィールドに一意の名前を入力します。 **[リージョン]** フィールドで、適切なリージョンを選択します。
4. セキュリティを適用する場合は、**[Restrict access to database (データベースへのアクセスを制限する)]** チェック ボックスをオンにします。
5. **[作成]** をクリックします。

## <a name="create-a-database-in-the-entities-pane-of-powerappscom"></a>powerapps.com の [エンティティ] ウィンドウでのデータベースの作成
1. [powerapps.com](https://web.powerapps.com) で、左側のナビゲーション ウィンドウの **[Common Data Service]** セクションを展開し、**[エンティティ]** をクリックまたはタップします。
2. **[Get started (開始する)]** をクリックします。 作成されるデータベースのアクセス モードはオープンになっています。

## <a name="open-and-restricted-databases"></a>オープンなデータベースと制限付きのデータベース
既定では、作成されるデータベースのアクセス モードはオープンになっています。 このモードでは、エンティティへのアクセスに関するセキュリティが適用されていません。 環境管理者は、データベースのアクセス モードを制限付きに設定できます。 このモードでは、アクセス許可のセットとロールに基づいて、エンティティへのアクセスに関するセキュリティが適用されます。

1. [管理センター](https://admin.powerapps.com)で、左側のナビゲーション ウィンドウの **[環境]** をクリックします。
2. 環境を選択します。
3. **[データベース]** タブで、次の手順のいずれかを実行します。
   * セキュリティを適用するには、**[Restrict access (アクセスを制限する)]** を選択します。
   * セキュリティを無効にするには、**[Open access (アクセスをオープンにする)]** を選択します。

## <a name="license-and-security-permissions"></a>ライセンスとセキュリティ アクセス許可
データベースを作成するには、選択した環境の管理者であり、適切なライセンスが割り当てられている必要があります。 そのような環境では、**[セキュリティ]** タブを使用して、他のユーザーのセキュリティ アクセス許可をさらに構成できます。詳細については、「[Configure database security (データベース セキュリティの構成)](database-security.md)」と「[Security model (セキュリティ モデル)](https://docs.microsoft.com/en-us/common-data-service/entity-reference/security-model)」を参照してください。

## <a name="privacy-notice"></a>プライバシーに関する声明
Microsoft PowerApps の Common Data Service では、Microsoft の診断システムにカスタム エンティティとフィールド名を収集して格納します。  収集した情報は、お客様向けの Common Data Service の改善に使用します。 作成者が作成するエンティティとフィールド名は、Microsoft PowerApps コミュニティ全体で共通するシナリオを理解したり、組織に関するスキーマなどの、サービスの標準エンティティの対象範囲のギャップを確認したりする場合に役立ちます。 このエンティティに関連するデータベース テーブルのデータに、Microsoft がアクセスまたは使用することはありません。また、データベースがプロビジョニングされているリージョン外にデータがレプリケートされることもありません。 ただし、カスタム エンティティとフィールド名はリージョン間でレプリケートされ、Microsoft のデータ保持ポリシーに基づいて削除される場合があります。 Microsoft はお客様のプライバシーを尊重いたします。詳細については、[Trust Center](https://www.microsoft.com/trustcenter/Privacy/default.aspx) を参照してください。

