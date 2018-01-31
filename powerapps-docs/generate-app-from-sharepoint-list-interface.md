---
title: "SharePoint リスト内からアプリを生成する | Microsoft Docs"
description: "SharePoint リスト内から、アイテムを管理する 3 つの画面から成るアプリを生成します。SharePoint サイトはオンプレミスとクラウドのどちらにあってもかまいません。"
services: 
suite: powerapps
documentationcenter: na
author: skjerland
manager: anneta
editor: 
tags: 
ms.service: powerapps
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 01/21/2017
ms.author: sharik
ms.openlocfilehash: 8ac8fb34f9cdeb0c9e0ce6172938cef33ecccbc5
ms.sourcegitcommit: 6afca7cb4234d3a60111c5950e7855106ff97e56
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2018
---
# <a name="generate-an-app-from-within-sharepoint-using-powerapps"></a>PowerApps を使用して、SharePoint 内からアプリを生成する



PowerApps で、ユーザーがカスタム SharePoint Online リスト内のアイテムを管理できるアプリを自動的に生成します。 アプリには 3 つの画面があり、ユーザーは次のことができます。

* リスト内のすべてのレコードを閲覧する (**BrowseScreen1**)
* 特定のレコードのすべてのフィールドを表示する (**DetailsScreen1**)
* レコードを作成または編集する (**EditScreen1**)

SharePoint Online コマンド バーからカスタム リストのアプリを作成する場合、アプリはそのリストのビューとして表示されます。 Web ブラウザーだけでなく、Windows Phone、iOS、または Android デバイスでもアプリを実行できます。

> [!IMPORTANT]
> PowerApps は全種類の SharePoint データをサポートするわけではありません。 詳細については、「[Known issues (既知の問題)](connections/connection-sharepoint-online.md#known-issues)」を参照してください。

## <a name="generate-an-app"></a>アプリを生成する
1. SharePoint Online でカスタム リストを開き、コマンド バーで **[PowerApps]**、**[アプリの作成]** の順にクリックまたはタップします。
   
    ![](./media/generate-app-from-sharepoint-list-interface/generate-new-app.png)
2. 表示されるパネルに、アプリの名前を入力し、**[作成]** をクリックまたはタップします。
   
    ![](./media/generate-app-from-sharepoint-list-interface/enter-app-name.png)
   
    新しいタブが Web ブラウザーに表示され、SharePoint リストに基づいて自動的に生成したアプリが表示されます。
   
    ![](./media/generate-app-from-sharepoint-list-interface/powerapp-studio-for-web.png)  
3. SharePoint リストのブラウザー タブをクリックまたはタップしてから、**[開く]** をクリックまたはタップします。
   
    > [!NOTE]
> ブラウザー ウィンドウを (F5 キーを押すなどして) 更新しないとアプリが開かない場合もあります。
   
    ![](./media/generate-app-from-sharepoint-list-interface/open-app-in-browser.png)
   
    別のブラウザー タブでアプリが開きます。
   
    ![](./media/generate-app-from-sharepoint-list-interface/open-app.png)

## <a name="manage-the-app"></a>アプリを管理する
![](./media/generate-app-from-sharepoint-list-interface/command-bar.png)

* **[Edit in PowerApps]\(PowerApps で編集する)** をクリックまたはタップすると、別のブラウザー タブでアプリが開き、Web 用の PowerApps Studio でこのアプリを更新できるようになります。
* **[Make this view public]\(このビューを公開する)** をクリックまたはタップすると、組織内の他のユーザーがビューを見ることができるようになります。 既定では、自分が作成したビューのみが表示されます。 他のユーザーがこのアプリを編集できるようにする場合は、[他のユーザーとアプリを共有して](share-app.md)から、**共同作成者**のアクセス許可を付与する必要があります。
* **[Remove this view]\(このビューを削除する)** をクリックまたはタップすると、SharePoint からビューが削除されますが、アプリは[削除](delete-app.md)しない限り PowerApps に残ります。

## <a name="next-steps"></a>次の手順
* リスト内のアイテムを追加または更新する方法については、「[Open app from a SharePoint Online list (SharePoint Online リストからアプリを開く)](open-app-embedded-in-sharepoint.md)」の「Manage the list using the app (アプリを使用してリストを管理する)」を参照してください。
* (既定で表示される) ブラウズ画面をカスタマイズするには、[レイアウトのカスタマイズ](customize-layout-sharepoint.md)に関するページを参照してください。
* 詳細画面または編集画面をカスタマイズするには、[フォームのカスタマイズ](customize-forms-sharepoint.md)に関するページを参照してください。
* このアプリを削除する場合は、SharePoint からビューを削除し、PowerApps から[アプリを削除](delete-app.md)します。

