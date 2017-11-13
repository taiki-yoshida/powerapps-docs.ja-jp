---
title: "ユーザー ライセンスの表示 | Microsoft Docs"
description: "管理者は PowerApps と Microsoft Flow のユーザー ライセンスの一覧をダウンロードできます"
services: 
suite: powerapps
documentationcenter: na
author: manasmamsft
manager: anneta
editor: 
tags: 
ms.service: powerapps
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/02/2017
ms.author: manasma
ms.openlocfilehash: ba60c227b287532f6abe2e2b2e88f6cbe7dd0cd3
ms.sourcegitcommit: 43be6a4e08849d522aabb6f767a81c092419babc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2017
---
# <a name="identify-powerapps-users-in-your-organization"></a>組織内の PowerApps ユーザーを特定する
Office 365 のグローバル管理者または Azure Active Directory のテナント管理者は、PowerApps、Microsoft Flow、またはその両方のライセンスが与えられているユーザーの一覧だけでなく、これらの製品のいずれかにアクセスしたユーザーの一覧もダウンロードできます。 一覧には、各ユーザーの名前、メール アドレス、ライセンスの種類、その他の情報などが含まれています。 たとえば、以下のようなユーザー情報です。

* PowerApps またはMicrosoft Flow の試用版のライセンスを所有している
* Office 365 ライセンスで両方の製品にアクセスできる
* Dynamics 365 ライセンスで両方の製品にアクセスできる
* PowerApps と Microsoft Flow プランからアクセスできる

## <a name="download-the-list-of-users"></a>ユーザーの一覧をダウンロードする
1. PowerApps 管理センターで、左端近くにある **[ユーザー ライセンス]** をクリックまたはタップします。
   
    **重要**: このオプションは、Office 365 のグローバル管理者と Azure Active Directory テナント管理者のみが使用できます。
   
    ![ファイルと共有](./media/admin-view-user-licenses/leftnav.png)
2. **[アクティブなユーザー ライセンスの一覧をダウンロード]** をクリックまたはタップします。
   
    ![ファイルと共有](./media/admin-view-user-licenses/download-list.png)
   
    ファイルのダウンロードに数分かかる場合があります。 数分待ってから、ダウンロードした .csv ファイルを Excel で開きます。
   
    **注**: ダウンロードが終了する前にウィンドウを閉じると、プロセスの再起動が必要になる場合があります。

この例は、さまざまな手段を通じて PowerApps と Microsoft Flow の両方のライセンスを所有している 2 人のユーザーを示しています。 Jane Doe は Office 365 のサブスクリプションでアクセスしており、John Doe は各製品の試用版のライセンスを取得済みです。

![ファイルと共有](./media/admin-view-user-licenses/table2.png)

この一覧には、PowerApps と Microsoft Flow のライセンスを所有しているが、これらに一度もアクセスしたことがないユーザーは含まれていません。 [Office 365 管理センター][1]から、すべてのユーザー ライセンスを表示できます。

ユーザーが組織を去った場合は、一覧の **[ユーザー名]** や **[電子メール アドレス]** などの列に **[不明]** と表示されます。 一覧に **[不明]** と表示されているが誰も組織から去ってない場合は、数分待ってから再び一覧をダウンロードします。

ユーザー ライセンスを追加するには、[Office 365 管理センター][1]を開きます。

<!--Reference links in article-->
[1]:https://support.office.com/article/Assign-or-remove-licenses-for-Office-365-for-business-997596b5-4173-4627-b915-36abac6786dc
