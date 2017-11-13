---
title: "データ損失防止 (DLP) ポリシー | Microsoft Docs"
description: "Microsoft PowerApps のデータ損失防止ポリシーの概要です。"
services: 
suite: powerapps
documentationcenter: na
author: msftman
manager: anneta
editor: 
tags: 
ms.service: powerapps
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/28/2016
ms.author: deonhe
ms.openlocfilehash: 67fb178a95131e041d0ea3ac5f3c2f24095505ed
ms.sourcegitcommit: 43be6a4e08849d522aabb6f767a81c092419babc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2017
---
# <a name="data-loss-prevention-dlp-policies"></a>データ損失防止 (DLP) ポリシー
## <a name="what-is-a-data-loss-prevention-policy"></a>データ損失防止ポリシーとは
組織のデータは、その成功に不可欠です。 そのデータは、意思決定のために容易に利用できる必要がありますが、アクセスすべきではないユーザーと共有されることがないように保護する必要があります。 このデータを保護するために、Microsoft PowerApps (以下 PowerApps) には、どのコンシューマー サービス/コネクタ固有のビジネス データを共有できるかを定義するポリシーを作成して適用する機能が用意されています。 データの共有方法を定義するこれらのポリシーは、データ損失防止 (DLP) ポリシーと呼ばれます。  

## <a name="why-create-a-dlp-policy"></a>DLP ポリシーを作成する理由
DLP ポリシーは、どのコンシューマー サービスのビジネス データを共有するかを明確に定義するために作成します。 たとえば、PowerApps を使用している組織で、SharePoint に保存されているビジネス データは Twitter フィードに自動的に発行したくないとします。 これを防ぐために、ツイートのソースとして SharePoint データが使用されることをブロックする DLP ポリシーを作成できます。

## <a name="benefits-of-a-dlp-policy"></a>DLP ポリシーの利点
* 組織全体でデータが一貫した方法で管理されていることを保証します。  
* 重要なビジネス データが誤ってソーシャル メディア サイトなどのサービスに発行されるのを防ぎます。   

## <a name="managing-dlp-policies"></a>DLP ポリシーの管理
**前提条件**  
DLP ポリシーを作成、編集、または削除するには、次の項目が必要です。

* 環境管理者またはテナント管理者としてのアクセス許可のいずれか。 アクセス許可の詳細については、[環境に関するトピック](environments-administration.md)を参照してください。

## <a name="create-a-dlp-policy"></a>DLP ポリシーを作成する
**前提条件**  
DLP ポリシーを作成するのには、少なくとも 1 つの環境へのアクセス許可が必要です。  

SharePoint データベースに保存されているデータが Twitter に公開されることを防止する DLP ポリシーを作成するには、次の手順に従います。  

1. [データ ポリシー] タブで、**[新しいポリシー]** リンクを選択します。  
   ![サインイン](./media/prevent-data-loss/create-policy-1.png)    
2. 表示されたページの上部にある **[データ ポリシー名]** に、DLP ポリシーの名前 (*Secure Data Access for Contoso*) を入力します。   
   ![サインイン](./media/prevent-data-loss/create-policy-2.png)  
3. **[適用先]** タブで[環境](environments-administration.md)を選択します。  
   ![サインイン](./media/prevent-data-loss/create-policy-3.png)  
4. **[データ グループ]** タブを選択します。  
   ![サインイン](./media/prevent-data-loss/create-policy-4.png)  
5. **[ビジネス データのみ]** グループ ボックス内にある **[+ 追加]** リンクを選択します。    
   ![サインイン](./media/prevent-data-loss/create-policy-5.png)  
6. **[サービスの追加]** ページで、**[SharePoint]** サービスと **[Salesforce]** サービスを選択します。  
   ![サインイン](./media/prevent-data-loss/create-policy-6.png)  
7. **[サービスの追加]** ボタンを選択して、ビジネス データの共有を許可されているサービスの一覧に選択したサービスを追加します。    
   ![サインイン](./media/prevent-data-loss/create-policy-7.png)  
8. **[ポリシーの保存]** を選択します。  
   ![サインイン](./media/prevent-data-loss/create-policy-8.png)  
9. しばらくすると、新しい DLP ポリシーが [データ損失防止ポリシー] の一覧に表示されます。  
   ![サインイン](./media/prevent-data-loss/create-policy-9.png)  
10. **(省略可能)** 新しい DLP ポリシーが利用可能になったことを知らせる電子メールやその他の通信をチームに送信します。

おつかれさまでした。これで、SharePoint と Salesforce 間でデータを共有し、他のサービスとのデータの共有をブロックする DLP ポリシーが作成されました。  

## <a name="find-a-dlp-policy"></a>DLP ポリシーを検索する
### <a name="admins"></a>管理者
管理者は、管理センターから検索機能を使用して、特定の DLP ポリシーを検索できます。  

**注:** 管理者は、すべての DLP ポリシーを発行して、組織内のユーザーが PowerApps を作成する前にポリシーを認識できるようにする必要があります。

### <a name="makers"></a>作成者
管理者権限はないが、組織の DLP ポリシーの詳細を知りたい場合は、管理者に問い合わせてください。 [作成者の環境に関するトピック](environments-overview.md)を参照することもできます。  

**注:** DLP ポリシーの編集と削除は、管理者のみが実行できます。  

## <a name="edit-a-dlp-policy"></a>DLP ポリシーを編集する
1. https://admin.powerapps.com に移動して管理センターを起動します。   
2. 起動した管理センターで、左側の **[データ ポリシー]** リンクを選択します。  
   ![サインイン](./media/prevent-data-loss/2.png)  
3. 既存の DLP ポリシーの一覧を検索して、編集するポリシーの横にある [編集] リンクを選択します。  
   ![サインイン](./media/prevent-data-loss/3.png)  
4. 必要な変更を加えます。 たとえば、グループ内の環境またはサービスを変更できます。  
5. **[ポリシーの保存]** を選択して変更を保存します。  
   ![サインイン](./media/prevent-data-loss/create-policy-8.png)  

これで、ポリシーが更新されました。 [データ損失防止ポリシー] の一覧でポリシーを検索し、そのプロパティを見直することで、変更内容がポリシーに反映されていることを確認できます。   

## <a name="delete-a-dlp-policy"></a>DLP ポリシーを削除する
1. https://admin.powerapps.com に移動して管理センターを起動します。    
2. 起動した管理センターで、左側の **[データ ポリシー]** リンクを選択します。  
   ![サインイン](./media/prevent-data-loss/2.png)  
3. 既存の DLP ポリシーの一覧を検索して、削除するポリシーの横にある [削除] リンクを選択します。  
   ![サインイン](./media/prevent-data-loss/3-delete.png)  
4. **[削除]** ボタンを選択して、ポリシーを削除することを確認します。  
   ![サインイン](./media/prevent-data-loss/4.png)  

これで、ポリシーが削除されました。 左側の **[データ ポリシー]** リンクし、ポリシーの一覧を見直すことで、[データ損失防止ポリシー] の一覧にポリシーの表示がなくなっていることを確認できます。   

## <a name="dlp-policy-permissions"></a>DLP ポリシーのアクセス許可
DLP ポリシーの作成と変更は、テナントと環境の管理者だけが実行できます。 アクセス許可の詳細については、[環境に関するトピック](environments-administration.md)を参照してください。  

## <a name="next-steps"></a>次の手順
* [環境に関する詳細](environments-administration.md)  
* [Microsoft PowerApps の詳細](getting-started.md)  
* [管理センターの詳細](introduction-to-the-admin-center.md)  

