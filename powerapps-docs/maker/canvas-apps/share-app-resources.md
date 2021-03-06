---
title: アプリで使用されているリソースを共有する | Microsoft Docs
description: アプリを共有しているときに、アプリで使用されているリソースを共有する方法について
services: ''
suite: powerapps
documentationcenter: na
author: archnair
manager: anneta
editor: ''
tags: ''
ms.service: powerapps
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 06/28/2016
ms.author: archanan
ms.openlocfilehash: 02df7f1df53842706bf6a41244f470f09de20c90
ms.sourcegitcommit: 59785e9e82da8f5bd459dcb5da3d5c18064b0899
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/22/2018
---
# <a name="share-app-resources"></a>アプリのリソースの共有
[アプリを共有](share-app.md)する前に、依存するリソースの種類 (たとえば以下のうちの 1 つまたは複数) を考慮してください。

* データ ソースへの接続
* オンプレミス データ ゲートウェイ
* カスタム コネクタ
* Excel ブックまたはその他のサービス
* フロー

これらのリソースの中には、アプリを共有すると自動的に共有されるものがあります。 その他のリソースでは、ユーザーまたはアプリを共有している相手が、アプリが期待どおりに動作するように、追加の手順を実行する必要があります。

組織全体で接続、カスタム コネクタおよびオンプレミス データ ゲートウェイを共有することもできます。

## <a name="connections"></a>接続
SQL Server などの接続の種類によっては、自動的に共有されるものもありますが、ユーザーがデータ ソースまたはアプリ内のソースへの接続を独自に作成する必要があるものもあります。

[powerapps.com](https://web.powerapps.com) では、接続を自動的に共有するかどうかを指定でき、共有アクセス許可を更新できます。 左側のナビゲーション バーで、**[管理]** をクリックまたはタップし、**[接続]** をクリックまたはタップして、[接続]をクリックまたはタップします。 **[共有]** タブが表示されたら、接続は自動的に共有されます。

  ![[接続の詳細] ページの [共有] タブ](./media/share-app-resources/shared-connections.png)

## <a name="on-premises-data-gateways"></a>オンプレミス データ ゲートウェイ
オンプレミス ソースからのデータを含むアプリを作成して共有する場合は、[オンプレミス データ ゲートウェイ](gateway-management.md) 自体およびそのゲートウェイへの接続のうち一定の種類が自動的に共有されます。 自動的に共有されていない接続はすべて、(前のセクションに表示されているとおり) 手動で共有でき、またユーザーが独自の接続を作成するようアプリに求めさせることができます。 接続またはゲートウェイが構成されている接続を表示する方法は次の通りです。

1. [powerapps.com](https://web.powerapps.com) を開き、左側のナビゲーション バーの **[管理]** をクリックまたはタップし、**[ゲートウェイ]** をクリックまたはタップします。
2. [ゲートウェイ]をクリックまたはタップして、**[接続]** タブをクリックまたはタップします。

> [!NOTE]
> 1 つ以上の接続を手動で共有する場合は、次の状況でもう一度共有する必要があるかもしれません。

* 既に共有しているアプリにオンプレミス データ ゲートウェイを追加します。
* オンプレミス データ ゲートウェイがあるアプリを共有したグループのセットまたはグループを変更します。

## <a name="custom-connectors"></a>カスタム コネクタ
カスタム コネクタを使用するアプリを共有するときに、アプリは自動的に共有されますが、ユーザーは独自の接続を作成する必要があります。

[powerapps.com](https://web.powerapps.com) で、カスタム コネクタのアクセス許可を表示または更新できます。 左側のナビゲーション バーで、**[管理]** をクリックまたはタップし、**[接続]** をクリックまたはタップして、右上隅の **[新しい接続]** をクリックまたはタップします。 **[カスタム]** をクリックまたはタップします。次にカスタム コネクタをクリックまたはタップして、詳細を表示します。

## <a name="excel-workbooks"></a>Excel ブック
共有しているアプリが、(クラウド ストレージ アカウントの Excel ブックなど) すべてのユーザーにアクセスがないデータを使用している場合は、[データを共有](share-app-data.md)します。

## <a name="flows"></a>フロー
フローを含むアプリを共有する場合、アプリを実行しているユーザーは、フローが依存しているすべての接続を確認または更新するように求められます。 さらに、フローを作成したユーザーのみが、パラメーターをカスタマイズすることができます。 たとえば、指定したアドレスにメールを送信するフローを作成できますが、他のユーザーはそのアドレスの変更ができません。

