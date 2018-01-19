---
title: "API コネクタの概要 | Microsoft Docs"
description: "ISV と SaaS サービス所有者は、コネクタを作成し、Microsoft の認定を受けることができます。"
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
ms.openlocfilehash: 74bac3b0f5bad2b95ab9b6b312fc5209bf5da3a2
ms.sourcegitcommit: 33099e6197c0139679cd08c42e9e2a5717904c92
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/12/2018
---
# <a name="api-connector-overview-powerapps"></a>API コネクタの概要 (PowerApps)
**API コネクタ**は、REST API のOpenAPI (Swagger) ベースのラッパーであり、基になるサービスが [Microsoft Flow](https://flow.microsoft.com)[PowerApps](https://powerapps.microsoft.com)、および [Logic Apps](https://docs.microsoft.com/azure/logic-apps/) と通信できるようにします。 それは、ユーザーが自分のアカウントを接続し、作成済みの**トリガー**と**アクション**のセットを活用して、アプリとワークフローを作成する方法を提供します。

**独立系ソフトウェア ベンダー (ISV)** または **SaaS サービス所有者**は、ユーザー向けの幅広いビジネスと生産性向上のシナリオを可能にするコネクタを作成することができます。 コネクタは、限定された統合の範囲を超えて、提供するサービスのリーチ、見つけやすさ、および利用を拡大することを支援します。

## <a name="requirements"></a>要件
コネクタを作成して提出するには、サービスが次の要件を満たしている必要があります。

* Microsoft Flow、PowerApps、および Logic Apps に十分に適合するビジネス ユーザー向けのシナリオであること
* 安定した REST API で公開されるサービスであること

## <a name="build-your-connector"></a>コネクタを作成する
API コネクタを作成するための最初の手順は、完全に機能するカスタム コネクタを作成することです。 カスタム コネクタは API コネクタとまったく同じように動作しますが、それを利用できるのは、作者と作成者のテナント内の特定のユーザーに限られています。

コネクタを作成するプロセスには、複数の手順が含まれています。

![API コネクタの作成手順](./media/api-connectors-overview/authoring-steps.png)

詳細については、[API コネクタの開発方法](api-connector-dev.md)に関するページを参照してください。

## <a name="submit-for-certification"></a>認定を受けるために提出する
コネクタを作成したら、認定を受けるために提出します。 Microsoft は、サード パーティ認定プロセスの一環として、コネクタを公開する前に審査を実施します。

このプロセスでは、Microsoft Flow と PowerApps でコネクタの機能を検証し、技術とコンテンツのコンプライアンスをチェックします。

詳細については、[認定と公開のためにコネクタを提出するプロセス](api-connector-submission.md)に関するページを参照してください。

## <a name="get-support"></a>サポートの要求
研修と開発のサポートを受けるには、[ condevhelp@microsoft.com](mailto:condevhelp@microsoft.com) 宛に電子メールをお送りください。このアカウントは、アクティブに監視され、管理されています。 開発者からの問い合わせとインシデントは、ただちに適切なチームに転送されます。

