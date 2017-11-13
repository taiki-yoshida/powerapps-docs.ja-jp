---
title: "サンプル アプリを使用する | Microsoft Docs"
description: "powerapps.com でサンプル アプリを使用するための詳しい手順。"
services: 
suite: powerapps
documentationcenter: na
author: linhtranms
manager: anneta
editor: 
tags: 
ms.service: powerapps
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/25/2016
ms.author: litran
ms.openlocfilehash: 7794f1ee28898016d3e8d4ac855f6ae1cf2090c7
ms.sourcegitcommit: 43be6a4e08849d522aabb6f767a81c092419babc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2017
---
# <a name="use-a-sample-app"></a>サンプル アプリを使用する
[powerapps.com](http://web.powerapps.com) でサンプル アプリを使用して、設計の可能性を探り、独自のアプリを開発する際に適用できる概念を見つけます。 各サンプル アプリでは、架空のデータを使用して、実際のシナリオを紹介します。

![](./media/open-and-run-a-sample-app/portal-home.png)

たとえば、**Cost Estimator** では、特定の大きさの部屋に床材を設置する際にかかるコストを見積もるための予定を作成できます。 住所や面積などの詳細を入力し、割引と税率に基づいて料金を算出します。 予定の一覧をフィルター処理し、見積もりが作成された予定、見積もりが作成されていない予定、またはすべての予定を表示します。

## <a name="open-the-app"></a>アプリの開始
1. [powerapps.com](https://web.powerapps.com) にサインインし、サンプル アプリの一覧にある **[Cost Estimator (コストの見積もり)]** をクリックまたはタップします。
   
    ![](./media/open-and-run-a-sample-app/app-tile.png)
2. **[Open for phone (スマートフォン用に開く)]** をクリックまたはタップしてスマートフォンで表示されるようにアプリを表示してから、**[Allow (許可)]** をクリックまたはタップしてデバイスのカメラの使用を許可します。
   
    アプリには、予定を作成するためのデータのほか、特定の大きさの部屋に特定の床材を設置する際にかかるコストを見積もるためのサンプル データが含まれています。
   
    ![](./media/open-and-run-a-sample-app/cost_estimator_home.png)

## <a name="make-and-view-an-appointment"></a>予定の作成と表示
1. **[+]** をクリックまたはタップし、見積もりの予定を作成します。
   
    ![](./media/open-and-run-a-sample-app/cost_estimator_add.png)
2. 詳細を入力し、**[Save job (ジョブの保存)]** をクリックまたはタップします。
   
    ![](./media/open-and-run-a-sample-app/cost_estimator_new.png)
   
    作成した予定が、予定の一覧に表示されます。
   
    ![](./media/open-and-run-a-sample-app/new_job_added.png)
3. 予定 (先ほど作成したものなど) をクリックまたはタップし、場所の地図などの詳細を表示します。
   
    ![](./media/open-and-run-a-sample-app/job_details.png)
   
    **注**: 予定は、右上隅のごみ箱アイコンをクリックまたはタップすることで削除できます。
   
    ![](./media/open-and-run-a-sample-app/job_delete.png)

## <a name="create-an-estimate"></a>見積もりの作成
1. 予定の詳細のページで、**[Begin Estimate (見積もりの開始)]** をクリックまたはタップします。
   
    ![](./media/open-and-run-a-sample-app/begin_estimate.png)
2. **[Name (名前)]**、**[Length (長さ)]**、**[Width (幅)]** などの部屋に関する必要な情報を入力し、**[Select flooring style (床のスタイルの選択)]** をクリックまたはタップします。
   
    ![](./media/open-and-run-a-sample-app/dimensions.png)
   
    床材のカテゴリの一覧が表示されます。
   
    ![](./media/open-and-run-a-sample-app/select_flooring_type.png)
3. **[Carpet (カーペット)]** をクリックまたはタップしてから、**[Caserta Sky Grey (カゼルタ スカイ グレー)]** をクリックまたはタップします。
   
    ![](./media/open-and-run-a-sample-app/carpet.png)
4. カメラが付いたデバイスでアプリを使用している場合、**[Add photos (写真の追加)]** をクリックまたはタップします。
   
    ![](./media/open-and-run-a-sample-app/add_photos.png)
5. 1 つ以上の写真を撮り、**[Done (完了)]** をクリックまたはタップします。
   
    ![](./media/open-and-run-a-sample-app/take_photos.png)

## <a name="finish-and-submit-an-estimate"></a>見積もりの完了と送信
1. **[Review Estimate (見積もりの確認)]** をクリックまたはタップします。
   
    ![](./media/open-and-run-a-sample-app/review_estimate.png)
2. (省略可能) **[Price adjustment (価格調整)]** と **[Tax (税)]** のレートを指定します。
3. 署名を追加してから、**[Submit estimate (見積もりを送信する)]** をクリックまたはタップします。
   
    ![](./media/open-and-run-a-sample-app/submit_estimate.png)
   
    ブラウザーの設定で許可されている場合、既定のメール クライアントが開き、メッセージに見積もりに関する情報が含まれます。
   
    ![](./media/open-and-run-a-sample-app/email.png)
   
    PowerApps の画面には、見積もりが送信されたことが示されます。
   
    ![](./media/open-and-run-a-sample-app/done.png)
4. **[Done (完了)]** をクリックまたはタップし、予定の一覧に戻ります。
   
    見積もりを完了した予定は緑色になります。これは、予定がクローズされたことを示します。
   
    ![](./media/open-and-run-a-sample-app/estimate_done.png)
5. (省略可能) 左上隅にあるフィルター アイコンをクリックまたはタップし、状態 (オープンまたはクローズ) で一覧をフィルター処理するか、すべての予定を表示します。

