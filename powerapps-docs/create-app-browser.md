---
title: "Web ブラウザーでのアプリの作成と編集 | Microsoft Docs"
description: "Web 用の PowerApps Studio を使用して、ブラウザーでアプリを作成し、編集します。"
services: 
suite: powerapps
documentationcenter: na
author: karthik-1
manager: anneta
editor: 
tags: 
ms.service: powerapps
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/06/2017
ms.author: karthikb
ms.openlocfilehash: 3c675e84f03e008a7f478d358a99fe3fff602002
ms.sourcegitcommit: 43be6a4e08849d522aabb6f767a81c092419babc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2017
---
# <a name="create-or-edit-apps-in-powerapps-studio-for-web"></a>Web 用の PowerApps Studio でのアプリの作成または編集
Windows または他のプラットフォームのブラウザー ウィンドウで開く Web 用の PowerApps Studio で、アプリの作成と編集を行います。

**前提条件**

* PowerApps に[サインアップ](signup-for-powerapps.md)。
* Windows または Mac 搭載のコンピューターの Microsoft Edge、Google Chrome、または Internet Explorer 11。

## <a name="open-powerapps-studio-for-web"></a>Web 用の PowerApps Studio を開く
1. [powerapps.com](http://go.microsoft.com/fwlink/p/?LinkId=708209) にサインインします。
2. 左下隅で **[新しいアプリ]** をクリックまたはタップします。
   
    ![左側のナビゲーション バーの新しいアプリ](./media/create-app-browser/left-nav.png)

Web 用の PowerApps Studio がブラウザーの新しいタブで開き、PowerApps Studio for Windows と同じ方法でアプリの作成と編集を行うことができます。

## <a name="next-steps"></a>次の手順
* [Excel](get-started-create-from-data.md) や [SharePoint](app-from-sharepoint.md) などのデータからアプリを自動的に生成します。
* [コントロールを追加してそのプロパティを設定](add-configure-controls.md)する方法を確認します。アプリの体裁と動作は、そのプロパティによって決まります。
* [アプリを最初から作成](get-started-create-from-blank.md)します。

## <a name="known-limitations"></a>既知の制限
1. **接続を作成する。**
   
    サービス認証が必要なデータソースへの[接続を作成する](add-manage-connections.md)には、[powerapps.com](https://web.powerapps.com) で行ってから、Web 用の PowerApps Studio でアプリに[その接続を追加](add-data-connection.md)します。
2. **ローカルのアプリを編集して保存する**。
   
    最良の結果を得るには、PowerApps Studio for Windows を使用してローカルのアプリを編集し、保存します。 ブラウザーではローカルのアプリに変更を保存することはできません。開いたファイルを置き換える代わりに新しいファイルを保存する必要があります。
3. **シグナル関数を使用する。**
   
    **[Acceleration および Compass](functions/signals.md)**関数は、公開されたアプリでは正確な値を返しますが、ブラウザーでアプリを作成または変更している場合にはゼロ値を返します。
4. **データをエクスポートおよびインポートする。**
   
    発行されたアプリでは[データをエクスポートおよびインポート](controls/control-export-import.md)できますが、ブラウザーでアプリを作成または変更している場合はできません。
5. **2 つのセッション間でコントロールをコピーする。**
   
    Web 用の PowerApps Studio のセッション間ではコントロールをコピーできません。

