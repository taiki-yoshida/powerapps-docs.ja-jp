---
title: "SharePoint リストのデータを管理するアプリの生成 | Microsoft Docs"
description: "SharePoint リストのデータを管理する 3 つの画面から成るアプリを作成します。SharePoint サイトはオンプレミスとクラウドのどちらにあってもかまいません。"
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
ms.date: 06/05/2017
ms.author: sharik
ms.openlocfilehash: 5d47366fafa137d8e5b0311f8820b11ff60f648a
ms.sourcegitcommit: 43be6a4e08849d522aabb6f767a81c092419babc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2017
---
# <a name="generate-an-app-to-manage-data-in-a-sharepoint-list"></a>SharePoint リストのデータを管理するアプリの生成
[!VIDEO nb:cid:UUID:34ccfd46-7826-49ce-90d8-cf6a144b6968]


PowerApps で、SharePoint リストのデータを管理する 3 つの画面から成るアプリを自動的に作成します。SharePoint サイトはオンプレミスとクラウドのどちらにあってもかまいません。

既定では、レコードを閲覧する画面、レコードの詳細を表示する画面、レコードを作成または更新する画面が、生成されたすべてのアプリに備わっています。 各画面の最初のレイアウトとコンテンツが自動的に決定されますが、大抵の場合は、ニーズに応じてアプリをカスタマイズする必要があります。

PowerApps の基本的な事柄については、「[PowerApps の概要](getting-started.md)」を参照してください。

この記事の執筆時点の PowerApps では、カスタム リストはサポートされていますが、ライブラリはサポートされていません。 さらに、**選択**や**画像**など、数種類の列でデータを表示できます。ただし、このデータは更新できません。 詳細については、「[Known issues (既知の問題)](connections/connection-sharepoint-online.md#known-issues)」を参照してください。

**注:** いずれかの列名にスペースが含まれている場合、PowerApps では **"\_x0020\_"** と表示されます。 たとえば、**"Column Name"** は **"Column_x0020_Name"** と表示されます。

## <a name="specify-a-sharepoint-app"></a>SharePoint アプリの指定
1. [SharePoint への接続](connect-to-sharepoint.md)をまだ作成していない場合は作成します。
2. 次の方法の *いずれか* で、PowerApps を開きます。
   
   * [PowerApps Studio for Windows をインストール](http://aka.ms/powerappsinstall)して開きます。その後、サインアップに使用したのと同じ資格情報を使ってサインインします。 左端近くにある **[New (新規)]** をクリックまたはタップします。
     
       ![[File (ファイル)] メニューの [New (新規)] オプション](./media/app-from-sharepoint/file-menu.png)
   * ブラウザーで [PowerApps Studio for the web を開き](https://create.powerapps.com/api/start)ます。
     
       PowerApps Studio for the web のプレビュー リリースでサポートされているブラウザーと制限の一覧については、「[Create or edit apps in a browser (ブラウザーでのアプリの作成または編集)](create-app-browser.md)」を参照してください。
3. **[データを使用して開始]** で、SharePoint タイルの **[携帯電話レイアウト]** をクリックまたはタップします。
   
    ![](./media/app-from-sharepoint/sharepoint-tile.png)

## <a name="specify-a-site-and-a-list"></a>サイトとリストの指定
1. **[Connect to a SharePoint site (SharePoint サイトに接続する)]** で、使用するリストが含まれたサイトへの URL を入力または貼り付けます。その後、**[Go (移動)]** をクリックまたはタップします。
   
    **注**: URL に特定のリストを含めないようにしてください。
   
    ![](./media/app-from-sharepoint/specify-site.png)
2. **[Choose a list (リストの選択)]** で、使用するリストの名前をクリックまたはタップします。
   
    並べ替えボタンをクリックまたはタップすることで、リスト名をアルファベット順で並べ替えることができます。
   
    ![](./media/app-from-sharepoint/sort-button.png)
   
    検索ボックスに 1 つ以上の文字を入力するか貼り付けるかして、指定したテキストが含まれたリスト名のみを表示することもできます。
   
    ![](./media/app-from-sharepoint/choose-list.png)
   
    すべての種類のリストが既定で表示されるわけではありません。 使用する目的のリストの名前が表示されていない場合は、一番下までスクロールし、**[カスタム リスト名を入力]** と示されているボックスにリスト名を入力します。
   
    ![](./media/app-from-sharepoint/custom-list.png)
3. **[Connect (接続)]** をクリックまたはタップして、アプリを生成します。
   
    ![[Connect (接続)] ボタン](./media/app-from-sharepoint/connect-button.png)
4. クイック ツアーの開始を求められたら、**[Next (次へ)]** をクリックまたはタップし、PowerApps インターフェイスの基本事項について確認します (または、**[Skip (スキップ)]** をクリックまたはタップします)。
   
    ![クイック ツアーの最初の画面](./media/app-from-sharepoint/quick-tour.png)
   
    クイック ツアーは後からいつでも開始できます。右上隅の疑問符アイコンをクリックまたはタップし、**[Take the intro tour (クイック ツアーの開始)]** をクリックまたはタップしてください。

## <a name="next-steps"></a>次の手順
* 生成したアプリを保存するには、Ctrl+S キーを押します。
* (既定で表示される) ブラウズ画面をカスタマイズするには、[レイアウトのカスタマイズ](customize-layout-sharepoint.md)に関するページを参照してください。
* 詳細画面または編集画面をカスタマイズするには、[フォームのカスタマイズ](customize-forms-sharepoint.md)に関するページを参照してください。

