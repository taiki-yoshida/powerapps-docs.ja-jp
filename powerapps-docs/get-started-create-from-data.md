---
title: "Excel データからアプリを生成する | Microsoft Docs"
description: "クラウド内の Excel ファイルをベースにしてアプリを自動的に作成し、カスタマイズして、その動作を詳しく見ていきます。"
services: 
suite: powerapps
documentationcenter: na
author: karthik-1
manager: anneta
editor: 
tags: 
ms.service: powerapps
ms.devlang: na
ms.topic: get-started-article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/16/2016
ms.author: sharik
ms.openlocfilehash: cf90156292985e58e2d68d2828d7c943b45facdf
ms.sourcegitcommit: 6afca7cb4234d3a60111c5950e7855106ff97e56
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2018
---
# <a name="generate-an-app-from-excel-data"></a>Excel データからアプリを生成する
OneDrive などのクラウド ストレージ アカウントにアップロードした Excel ファイル内のデータに基づいて自動的にアプリを作成します。 アプリを生成した後、ニーズに合わせてカスタマイズし、実行して期待どおりに動作するかどうかを確認します。

既定では、生成されたアプリには次の 3 つの画面があります。

* **BrowseScreen1** では、1 つまたは複数のフィールドのサブセット、検索バー、並べ替えボタンが表示され、ユーザーが特定のレコードを見つけやすくなっています。
* **DetailsScreen1** では、特定のレコードについてさらに多く (またはすべて) のフィールドが表示されます。
* **EditScreen1** では、ユーザーがレコードを作成または更新して変更内容を保存できる UI 要素が表示されます。

> [!NOTE]
> [カスタム SharePoint リスト](app-from-sharepoint.md)に基づいてアプリを生成することもできます。

## <a name="prerequisites"></a>前提条件
* [PowerApps にサインアップ](signup-for-powerapps.md)し、次の手順のいずれかを実行します。
  * Windows 8、Windows 8.1 または Windows 10 搭載のコンピューターに [PowerApps Studio for Windows](http://aka.ms/powerappsinstall) をインストールします。
  * ブラウザーで [PowerApps Studio for web](create-app-browser.md) (プレビュー版) を開きます。
* サインアップに使用した資格情報で PowerApps にサインインします。
* このチュートリアルの手順に忠実に従うには、この [Excel ファイル](https://az787822.vo.msecnd.net/documentation/get-started-from-data/FlooringEstimates.xlsx)をダウンロードします。
  
    > [!IMPORTANT]
> データがテーブルとして書式設定されていれば、ご自身の Excel ファイルを使用できます。 詳細については、「[Excel テーブルを作成または削除する](https://support.office.com/en-us/article/Create-an-Excel-table-in-a-worksheet-E81AA349-B006-4F8A-9806-5AF9DF0AC664)」を参照してください。
* Excel ファイルを OneDrive や他の[クラウド ストレージ アカウント](connections/cloud-storage-blob-connections.md)にアップロードします。

## <a name="create-an-app"></a>アプリを作成する
1. PowerApps Studio の **[File (ファイル)]** メニュー (画面左側) の **[New (新規)]** をクリックまたはタップします。
   
    ![[ファイル] メニューの [新規] オプション](./media/get-started-create-from-data/file-new.png)
2. 次のいずれかの手順に従います。
   
   * クラウド ストレージ アカウントが **[Start with your data (データを使用して開始)]** の下に表示された場合は、**[電話レイアウト]** をクリックまたはタップします。
     
     ![データからアプリを作成するためのオプション](./media/get-started-create-from-data/create-from-data.png)
   * クラウド ストレージ アカウントが **[Start with your data (データを使用して開始)]** に表示されない場合は、タイルの行の末尾にある矢印をクリックします。 アカウントが接続の一覧に表示された場合は、そのエントリをクリックまたはタップします。
   * クラウド ストレージ アカウントが **[Start with your data (データを使用して開始)]** または接続の一覧に表示されない場合は、**[新しい接続]** をクリックまたはタップしてから、アカウントのエントリをクリックまたはタップします。 **[接続]** をクリックまたはタップし、画面の指示に従って接続を構成します。
     
     ![OneDrive に接続](./media/get-started-create-from-data/connect-onedrive.png)
3. **[Choose an Excel file (Excel ファイルの選択)]** で **FlooringEstimates.xlsx** を参照してクリックまたはタップします。
   
    ![FlooringEstimates Excel ファイル](./media/get-started-create-from-data/choose-spreadsheet.png)  
4. **[Choose a table (テーブルの選択)]** で **[FlooringEstimates]** をクリックまたはタップします。  
   
    ![FlooringEstimates テーブルを選択](./media/get-started-create-from-data/choose-table.png)
5. **[Connect (接続)]** をクリックまたはタップして、アプリを生成します。
6. クイック ツアーの開始を求められたら、**[次へ]** をクリックまたはタップし、PowerApps ユーザー インターフェイスの基本事項について確認します (あるいは、**[スキップ]** をクリックまたはタップします)。
   
    ![[次へ] をクリックしてツアーを開始](./media/get-started-create-from-data/quick-tour.png)
   
    > [!NOTE]
> クイック ツアーは後からいつでも開始できます。右上隅の疑問符アイコンをクリックまたはタップし、**[Take the intro tour (クイック ツアーの開始)]** をクリックまたはタップしてください。

## <a name="change-the-gallery-layout"></a>ギャラリー レイアウトの変更
アプリはデータに基づいた既定のレイアウトで作成されますが、ニーズに合わせてギャラリーのレイアウトをカスタマイズできます。

1. 左側のナビゲーション バーで、右上のアイコンをクリックまたはタップしてサムネイル表示に切り替えます。
   
    ![表示の切り替え](./media/get-started-create-from-data/toggle-view.png)
2. 一番上のサムネイルをクリックまたはタップし、ブラウズ画面 (**BrowseScreen1**) を選択します。
3. 最初のイメージなど、ギャラリー内の任意の場所をクリックまたはタップします。
   
    ![イメージの選択](./media/get-started-create-from-data/select-image.png)
4. 右側のウィンドウで、**[レイアウト]** リストを開き、イメージ、タイトル、サブタイトルを含むレイアウトをクリックまたはタップします。
   
    ![レイアウトを選択する](./media/get-started-create-from-data/select-layout.png)
   
    選択内容に基づいて、アプリのレイアウトが変更されます。
   
    ![BrowseScreen1 と新しいレイアウト](./media/get-started-create-from-data/browse-layout.png)

## <a name="change-the-data-that-appears"></a>表示されるデータを変更する
1. **[アイテムの検索]** で **[Carpet]** (カーペット) をクリックまたはタップして、**ラベル** コントロールを選択します。
   
   関連するリストが右側のウィンドウで強調表示されます。
   
   ![1 つ目のラベルを選択](./media/get-started-create-from-data/select-gallery-textbox.png)
2. 右側のウィンドウで、強調表示されたリストを開いてから、**[名前]** をクリックまたはタップします。
   
    ![1 つ目のラベルを設定](./media/get-started-create-from-data/set-gallery-textbox.png)
3. 下の一覧を開いてから、**[カテゴリ]** をクリックまたはタップします。
   
    ![カテゴリの設定](./media/get-started-create-from-data/set-category.png)
   
    **BrowseScreen1** を変更し、名前と各レコードのカテゴリを表示します。
   
    ![BrowseScreen1 と新しいコンテンツ](./media/get-started-create-from-data/browse-content.png)
   
    > [!NOTE]
> 既定では、マウスホイールまたはタッチ スクリーン上での上下方向のスワイプ操作によって、リスト (ギャラリー) をスクロールすることができます。 トラックパッドまたはホイールなしのマウスを使用するには、ギャラリーを選択し、プロパティの一覧で **[スクロール バーの表示]** をクリックまたはタップしてから、数式バーの **false** を **true** に置換します。

## <a name="change-the-order-of-fields-in-a-form"></a>フォームのフィールドの順序を変更する
1. 左側のナビゲーション バーで中央のサムネイルをクリックまたはタップし、詳細画面 (**DetailsScreen1**) を開きます。
   
    ![DetailScreen 1 のサムネイル](./media/get-started-create-from-data/detail-screen-thumbnail.png)
2. 画像をクリックまたはタップするとオプションが表示され、フォームをカスタマイズできます。
   
    ![カードを選択](./media/get-started-create-from-data/select-card.png)
3. 右側のウィンドウで、**[名前]** フィールドをリストの先頭にドラッグします。
   
    ![カードを移動する](./media/get-started-create-from-data/move-card.png)
   
    画面を更新して変更を反映します。
   
    ![画面の上部にある名前](./media/get-started-create-from-data/name-first.png)

## <a name="change-a-control"></a>コントロールの変更
1. 左側のナビゲーション バーで一番下のサムネイルをクリックまたはタップし、編集画面 (**EditScreen1**) を開きます。
   
    ![EditScreen1 のサムネイル](./media/get-started-create-from-data/edit-screen-thumbnail.png)
2. **[概要]** をクリックまたはタップします。
   
    この手順では、[概要] カードを選択します。 各カードには、カードの目的を説明するテキストが含まれています。 カードのコントロールをカスタマイズすることもできます。 詳細については、「[Card control in PowerApps (PowerApps でのカードのコントロール)](controls/control-card.md)」をご覧ください。
   
    ![概要カードを選択](./media/get-started-create-from-data/select-overview.png)
3. 右側のウィンドウで、カードの下矢印をクリックまたはタップしてスクロールし、**[複数行テキストの編集]** をクリックまたはタップします。
   
    この手順では、テキストを表示できる大きさのコントロールに各製品の概要を表示する方法を説明します。
   
    ![カードの変更](./media/get-started-create-from-data/card-selector.png)

## <a name="run-the-app"></a>アプリの実行
アプリをカスタマイズする場合は、プレビュー モードでアプリを実行して変更をテストしてください。

1. 左側のナビゲーション バーで一番上のサムネイルをクリックまたはタップし、ブラウズ画面 (**BrowseScreen1**) を開きます。
2. F5 キーを押すか、右上隅の **[再生]** ボタンをクリックまたはタップして、プレビュー モードを開始します。
   
    ![プレビュー アイコン](./media/get-started-create-from-data/open-preview.png)
3. **BrowseScreen1** で、レコードの右側の矢印をタップまたはクリックして、詳細画面 (**DetailsScreen1**) のレコードを表示します。
   
    ![BrowseScreen1 で矢印を選択](./media/get-started-create-from-data/select-record.png)
4. **DetailsScreen1** で、右上隅にある鉛筆アイコンをクリックまたはタップして、編集画面 (**EditScreen1**) のレコードを表示します。
   
    ![レコードを編集](./media/get-started-create-from-data/edit-record.png)
5. **EditScreen1** で、少なくとも 1 つのフィールドの情報を変更し、右上隅のチェック マークをクリックまたはタップして変更内容を保存します。
   
    ![EditScreen1 で変更を保存](./media/get-started-create-from-data/save-record.png)
6. Esc キーを押して (またはタイトル バーの下にある閉じるアイコンをクリックまたはタップして) プレビュー モードを終了します。
   
    ![プレビュー モードの終了](./media/get-started-create-from-data/close-preview.png)

### <a name="known-limitations"></a>既知の制限
お客様の組織内の Excel データを共有する方法の詳細については、[これらの制限をご確認ください](connections/cloud-storage-blob-connections.md#sharing-excel-tables)。

## <a name="next-steps"></a>次の手順
* アプリを保存して他のデバイスから実行できるようにするには、Ctrl + S キーを押します。
* データからアプリを生成する方法を学習しました。これで[アプリを最初から作成](get-started-create-from-blank.md)できます。
* 他のユーザーが実行できるように[アプリを共有](share-app.md)する。

