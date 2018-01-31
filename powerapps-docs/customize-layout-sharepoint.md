---
title: "ギャラリー レイアウトのカスタマイズ | Microsoft Docs"
description: "表示するコントロールと各コントロールに表示するフィールド、さらにレコードの並べ替えと検索に使用する列を指定します。"
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
ms.date: 05/02/2017
ms.author: sharik
ms.openlocfilehash: ce0f0693298977ca991636d0a9bf18e238e8368e
ms.sourcegitcommit: 6afca7cb4234d3a60111c5950e7855106ff97e56
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2018
---
# <a name="customize-a-gallery-layout-in-powerapps"></a>PowerApps でのギャラリー レイアウトのカスタマイズ
PowerApps で自動的にアプリを生成したら、既定で表示されるブラウズ画面をカスタマイズしましょう。 使用するレイアウトと表示する列、さらにレコードの並べ替えとフィルター処理に使用する列を指定します。

* アプリを自動的に生成する方法については、「[Generate an app to manage data in a SharePoint list (SharePoint リストのデータを管理するアプリを生成する)](app-from-sharepoint.md)」を参照してください。
* PowerApps の基本的な事柄については、「[PowerApps の概要](getting-started.md)」を参照してください。

## <a name="prerequisites"></a>前提条件
このチュートリアルは、概念全般を理解する目的でのみご覧いただいても、目的を果たすために各手順を忠実に実行していただいてもかまいません。

1. PowerApps から SharePoint への[接続を作成](connect-to-sharepoint.md)します。
2. 以下の列を含んだ **AppGen** という名前の SharePoint リストを作成します。
   
    ![SharePoint のサンプル列](./media/customize-layout-sharepoint/list-columns.png)
3. 作成したリストに以下の項目を追加します。
   
    ![サンプル データ](./media/customize-layout-sharepoint/sample-data.png)
4. 作成したリストに基づいて[アプリを自動的に生成](app-from-sharepoint.md)します。
5. 左側のナビゲーション バーで、右上のアイコンをクリックまたはタップしてサムネイル表示に切り替えます。
   
    ![表示の切り替え](./media/customize-layout-sharepoint/toggle-view.png)

## <a name="customize-the-gallery"></a>ギャラリーのカスタマイズ
1. 左側のナビゲーション バーで一番上のサムネイルをクリックまたはタップし、**BrowseScreen1** を選択します。
   
    ![BrowseScreen1 のサムネイル](./media/customize-layout-sharepoint/browse-thumbnail.png)
   
    **BrowseScreen1** に、SharePoint リスト内の各項目の **AccountID** と **Title** が表示されます。
   
    ![ブラウズ画面にタイトルとアカウント ID が表示される](./media/customize-layout-sharepoint/browse-accountid.png)
   
    次にそれぞれの項目に関して、**AccountID** ではなく **OrderDate** が表示されるように指定します。
2. 画面上の最初の項目の **AccountID** をクリックまたはタップします。
   
    UI 要素 (コントロール) をクリックまたはタップして選択すると、コントロールの周囲に選択状態を示す境界線とサイズ変更ハンドルが表示されます。
   
    ![最初の項目を選択](./media/customize-layout-sharepoint/select-body.png)
3. 右側のウィンドウで、**[Title1]** リストを開いてから、**[OrderDate]** をクリックまたはタップします。
   
    ![タイトルを表示](./media/customize-layout-sharepoint/bind-data.png)
   
    **BrowseScreen1** に変更が反映されます。
   
    ![日付を含んだレイアウト](./media/customize-layout-sharepoint/browse-dates.png)

ギャラリーについて詳しくは、「[PowerApps の項目の一覧の表示](add-gallery.md)」をご覧ください。

## <a name="set-the-sort-and-search-columns"></a>並べ替え列と検索列の設定
1. 1 つ目を除く任意のレコードをクリックまたはタップして**ギャラリー** コントロールを選択します。
   
    ![ギャラリーを選択](./media/customize-layout-sharepoint/select-gallery.png)
2. 左上隅のプロパティ一覧に **Items** が表示されていることを確認します。
   
    ![Items プロパティ](./media/customize-layout-sharepoint/items-property.png)
   
    このプロパティの値は数式バーに表示され、画面に表示されるデータのソースに加え、フィルター列と並べ替え列を左右します。
   
    たとえば、数式バーには次のような式が既定で表示されます。
   
    ![既定の Items プロパティ](./media/customize-layout-sharepoint/default-items.png)
   
    ユーザーはこの式に基づいて、**AccountID** 列が 1 つ以上の文字で始まるレコードのみを表示することができます。
   
    ![既定の検索列](./media/customize-layout-sharepoint/default-search.png)
   
    たとえばユーザーがアルファベットの「A」を検索バーに入力すると、Europa のレコードが画面に表示されます。 指定した検索条件に対してレコードのタイトルは一致しませんが、アカウント ID が一致します。 この手順の後半で、**Title** 列に基づいてレコードをフィルター処理するように式を変更します。
   
    ユーザーは、生成されたアプリの右上隅の並べ替えボタンをクリックまたはタップすることにより、アルファベットの昇順または降順でレコードを並べ替えることができます。 次の式は、**AccountID** 列に基づいてレコードを並べ替えるように指定しています。
   
    ![既定の並べ替え列](./media/customize-layout-sharepoint/default-sort.png)
   
    後からこの手順の中で、**Title** 列でレコードを並べ替えるように式を変更します。
3. 数式バーで、**AccountID** の両方のインスタンスを **Title** に置き換えます (2 つ目のインスタンスを囲んだ二重引用符を含む)。
   
    変更後の数式バーには、次のように式が設定されている必要があります。<br>
    **SortByColumns(Filter(AppGen, StartsWith(Title, TextSearchBox1.Text)), "Title", If(SortDescending1, Descending, Ascending))**
   
    > [!NOTE]
> これまでに行った操作によっては、**TextSearchBox** の後に表示される数字がさらに大きい場合があります。 ただし数式の機能には問題ありません。

## <a name="test-sorting-and-searching"></a>並べ替えと検索のテスト
1. F5 キーを押して (または右上隅の再生ボタンをクリックまたはタップして) プレビュー モードを開始します。
   
    ![プレビュー モードを開始](./media/customize-layout-sharepoint/open-preview.png)
2. **BrowseScreen1** の右上隅にある並べ替えボタンを少なくとも 1 回クリックまたはタップして、アルファベットに基づく表示順を昇順または降順に変更します。
   
    ![並べ替えボタンのテスト](./media/customize-layout-sharepoint/test-sort.png)
3. 検索ボックスに文字を入力すると、タイトルがその文字で始まるレコードのみが表示されます。
   
    ![検索バーのテスト](./media/customize-layout-sharepoint/test-search.png)
4. 検索バーからテキストをすべて削除し、Esc キーを押して (または PowerApps のタイトル バーの "*下*" にある閉じるアイコンをクリックまたはタップして) プレビュー モードを終了します。
   
    ![プレビュー モードの終了](./media/customize-layout-sharepoint/close-preview.png)

## <a name="change-the-title-of-the-screen"></a>画面のタイトルの変更
1. 画面のタイトルをクリックまたはタップして選択します。
   
    ![画面タイトルを選択](./media/customize-layout-sharepoint/select-screen-title.png)
2. プロパティの一覧に **Text** を表示した状態で、数式バーに目的の名前を二重引用符で囲んで入力します。
   
    ![画面タイトルの更新](./media/customize-layout-sharepoint/update-screen-title.png)
   
    **BrowseScreen1** に変更が反映されます。
   
    ![新しい画面タイトル](./media/customize-layout-sharepoint/new-screen-title.png)

## <a name="next-steps"></a>次の手順
* Ctrl + S キーを押して変更を保存する。
* フォームに表示されるフィールドの表示と非表示を変更したり表示順を変更したりして、アプリの[フォームをカスタマイズ](customize-forms-sharepoint.md)する。

