---
title: "Microsoft Teams にアプリを追加して開く | Microsoft Docs"
description: "Microsoft Teams にアプリを追加して開きます。"
services: 
suite: powerapps
documentationcenter: na
author: sarafankit
manager: anneta
editor: 
tags: 
ms.service: powerapps
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/20/2017
ms.author: ankitsar
ms.openlocfilehash: 64c14c7e3a6ab599aa14d2200679134cc3fcc7d2
ms.sourcegitcommit: 43be6a4e08849d522aabb6f767a81c092419babc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2017
---
# <a name="add-and-open-an-app-in-microsoft-teams"></a>Microsoft Teams にアプリを追加して開く
Microsoft Teams チャネルにアプリを追加すると、アプリの共有相手であるすべてのユーザーが、そのチャネル内からアプリを開くことができます。 自分で作成したアプリか、"**使用可能**" または "**編集可能**" のアクセス許可を持っているアプリを追加できます。また、ブラウザーまたは Microsoft Teams のデスクトップ アプリから、アプリを追加することも開くこともできます。

## <a name="add-an-app"></a>アプリを追加する
1. チームの他のメンバーと[アプリを共有](share-app.md)します。
2. Microsoft Teams で、チームとそのチームが使用するチャネルを選択します。
   
    ![](./media/open-app-embedded-in-teams/teams-select-channel.png)
3. **[+]** をクリックまたはタップしてタブを追加します。
   
    ![](./media/open-app-embedded-in-teams/teams-add-tab.png)
4. **[Add a tab]\(タブの追加\)** ダイアログ ボックスで、**[PowerApps]** をクリックまたはタップします。
   
    ![](./media/open-app-embedded-in-teams/add-a-tab.png)
5. 追加するアプリをクリックまたはタップします。
   
    **注**: 名前、作成者、または環境によってアプリを検索できます。
   
    ![](./media/open-app-embedded-in-teams/select-an-app.png)
6. **[保存]** ボタンをクリックまたはタップします。
   
    ![](./media/open-app-embedded-in-teams/save-tab.png)
   
    アプリがチャネルで使用可能になりました。
   
    ![](./media/open-app-embedded-in-teams/app-in-channel.png)

## <a name="open-an-app"></a>アプリを開く
1. Microsoft Teams で、チームと、アプリを含むチャネルを選択します。
   
    ![](./media/open-app-embedded-in-teams/teams-select-channel.png)
2. アプリの名前を表すタブをクリックまたはタップします。
   
    ![](./media/open-app-embedded-in-teams/open-tab.png)
   
    チャネルでアプリが開きます。
   
    ![](./media/open-app-embedded-in-teams/app-in-channel.png)

## <a name="known-issues"></a>既知の問題
Microsoft Teams のデスクトップ アプリでは:

* アプリは、セキュリティで保護された (https) 接続経由でイメージや .pdf ファイルなどのコンテンツを読み込む必要があります。
* すべてのセンサー (**Acceleration**、**Compass**、**Location** など) がサポートされているとは限りません。
* サポートされているオーディオ形式は、AAC、H264、OGG Vorbis、および WAV のみです。

