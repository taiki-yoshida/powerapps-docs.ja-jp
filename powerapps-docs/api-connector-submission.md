---
title: "API コネクタとして認定されるために提出する | Microsoft Docs"
description: "コネクタの認定を受けることで、Microsoft Flow、PowerApps、および Logic Apps のすべてのユーザーがそれを利用できるようになります。"
services: 
suite: powerapps
documentationcenter: na
author: asavaritayal
manager: anneta
editor: 
tags: 
ms.service: powerapps
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/06/2017
ms.author: astay
ms.openlocfilehash: 265fde7b8ce5d5521c53af35a2274409523282fe
ms.sourcegitcommit: 68eee592c351688e5d0bd458f33a70be507fa53f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2018
---
# <a name="submit-for-certification-as-an-api-connector-powerapps"></a>API コネクタとして認定されるために提出する (PowerApps)
弊社では、サード パーティ認定プロセスの一環として、コネクタを公開する前に審査を実施しています。 コネクタの認定を受けることで、Microsoft Flow、PowerApps、および Logic Apps のすべてのユーザーがそれを利用できるようになります。 認定基準と手順を次に示します。

## <a name="criteria"></a>基準
| 機能 | 詳細 | 必須または推奨 |
| --- | --- | --- |
| ビジネス向けのサービスとしてのソフトウェア (SaaS) |Microsoft Flow、PowerApps、および Logic Apps に十分に適合するビジネス ユーザー向けのシナリオであること |必須 |
| 認証の種類 |API は OAuth2、API キー、または基本認証をサポートしていること |必須 |
| サポート |お客様が支援を受けることができるサポートの連絡先が用意されていること |必須 |
| 可用性/アップタイム |アプリのアップタイムが少なくとも 99.9% であること |推奨 |

## <a name="submitting-your-connector"></a>コネクタを提出する
次の 3 つの単純な手順で、Microsoft Flow、PowerApps、および Logic Apps 向けのコネクタとしての認定を受けることができます。

1. **申請**
   
   * [認定申請を提出します。](https://go.microsoft.com/fwlink/?linkid=848754)
   * 機密保持契約書とパートナー契約書を受領します。 先に進むためには、署名付きの契約書が必要です。
   * 申請が基準を満たしているかどうかがチェックされます。 承認後に、認定を開始するための指示が通知されます。
2. **審査**
   
    審査を受けるための次の情報を認定担当者に提出します。 追加情報が必要な場合は、詳細について連絡があります。
   
   * 作成した API を記述している OpenAPI ファイル
   * icon.png ファイル (230 ピクセル四方の 160 以下のピクセルのロゴ、色付きの背景に白を推奨)
   * 16 進数のブランド カラー (icon ファイルの色付きの背景と一致)
   * 検証用のテスト アカウント
   * サポートの問い合わせ先
3. **公開**
   
    コネクタ機能とコンテンツの検証が終了したら、コネクタがすべての製品とリージョンでデプロイ用にステージングされます。 
   
    既定では、すべてのコネクタが "premium" として公開されます。 アプリが Azure に組み込まれている場合は、Office 365 Enterprise プランのすべてのユーザーに利用可能な “standard” のコネクタとして表示されているコネクタを使用して適用できます。 詳細については、指定の問い合わせ先にお尋ねください。

