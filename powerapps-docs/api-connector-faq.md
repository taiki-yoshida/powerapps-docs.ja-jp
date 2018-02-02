---
title: "API コネクタの FAQ | Microsoft Docs"
description: "要件、トリガー、およびその他の領域についての質問に対する回答を見つけます。"
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
ms.openlocfilehash: b945f2775e26327557255a75f18e87a638a9fe66
ms.sourcegitcommit: 68eee592c351688e5d0bd458f33a70be507fa53f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2018
---
# <a name="api-connector-faq-powerapps"></a>API コネクタの FAQ (PowerApps)
## <a name="requirements"></a>要件
**Q:** ISV でなければ、コネクタを作成することはできませんか。

**A:** コネクタをパブリックにリリースするには、基となるサービスを所有しているか、API を使用する明示的な権利を提示する必要があります。

**Q:** REST API なしでコネクタを作成できますか。

**A:** いいえ。 API コネクタを作成するには、サービスに対して安定した HTTP REST API をサポートする必要があります。

**Q:** サポートされている認証の種類は何ですか?

**A:** 次の標準認証をサポートしています。

* OAuth2.0 (Azure Active Directory を含みます)
* API キー
* 基本認証

## <a name="triggers"></a>トリガー
**Q:** webhook なしのトリガーを作成できますか。 

**A:** Microsoft Flow と Logic Apps 用の API コネクタでは、webhook ベースのトリガーのみを作成できます。 他の形式の実装のリクエストがある場合は、API に関する詳細と併せて [condevhelp@microsoft.com](mailto:condevhelp@microsoft.com) にお問い合わせください。

## <a name="miscellaneous"></a>その他
**Q:** 私の API では、動的ホストを使用します。 OpenAPI でこれを実装するにはどうすればよいですか。

**A:** API コネクタの機能では、動的ホストはサポートしていません。 開発とテストでは静的なホストを使用してください。 送信時に、動的な実装に関して Microsoft にお問い合わせください。

**Q:** Postman Collection V2 はサポートしていますか。

**A:**いいえ、Postman V2 は現在サポートされていません。

**Q:** OpenAPI 3.0 はサポートしていますか。

**A:** いいえ、現在サポートされている唯一のバージョンは OpenAPI 2.0 です。

