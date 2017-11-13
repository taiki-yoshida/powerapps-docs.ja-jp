---
title: "Common Data Service データベースを使用してアプリを生成する | Microsoft Docs"
description: "レコードを追加、更新、および削除するアプリを生成します。"
services: powerapps
documentationcenter: na
author: kfend
manager: kfend
editor: 
tags: 
ms.service: powerapps
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 12/06/2016
ms.author: kfend
ms.openlocfilehash: 7fffa909b42dfd23bc4b72d032a524df27d614aa
ms.sourcegitcommit: 43be6a4e08849d522aabb6f767a81c092419babc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2017
---
# <a name="generate-an-app-by-using-a-common-data-service-database"></a>Common Data Service データベースを使用してアプリを生成する
[!VIDEO nb:cid:UUID:6d7aa0a1-cd31-47c6-9a32-93b4e5476ece]


Common Data Service に格納されているデータを管理するアプリを自動的に生成することができます。 データの管理は、モデルに組み込まれている数多くの標準エンティティのいずれかで行うか、自分または同じ組織内の別のユーザーが作成したカスタム エンティティで行うことができます。

Common Data Service の基本的な事柄については、「[エンティティについて](data-platform-intro.md)」を参照してください。

このトピックでは、指定した単一のエンティティを基にアプリを自動的に生成する方法を説明します。 複数のエンティティを基にアプリを構築する方法については、「[アプリをゼロから作成](data-platform-create-app-scratch.md)」を参照してください。

Microsoft PowerApps によって生成されるすべてのアプリには、既定で次の 3 つの画面があります。

* ブラウズ画面。1 つ以上のフィールドのサブセット、検索バー、並べ替えボタンが表示され、特定のレコードをユーザーが見つけやすいようになっています。
* 詳細画面。特定のレコードについて、さらに多く (またはすべて) のフィールドが表示されます。
* 編集画面。ユーザーがレコードを作成または更新して変更内容を保存することのできる UI 要素が表示されます。

**注:** Common Data Service からアプリを生成する場合、SharePoint、Dynamics 365、Salesforce などのデータ ソースが利用できるので、PowerApps から接続を作成する必要はありません。 必要な作業は、アプリでの操作 (表示、管理、またはその両方) の対象となるエンティティを指定するだけです。

## <a name="generate-an-app"></a>アプリを生成する
1. Common Data Service データベースを作成します。 詳細については、「[Create a Common Data Service database (Common Data Service サービスの作成)](create-database.md)」を参照してください。
2. PowerApps Studio for Windows で **[ファイル]** メニュー (画面左側) の **[新規]** をクリックまたはタップします。
3. **[データを使用して開始]** の下の **[Common Data Service]** タイルで、**[携帯電話レイアウト]** をクリックまたはタップします。
4. **[Choose an entity (エンティティの選択)]** で、**Contact** エンティティをクリックまたはタップします。
5. **[Connect (接続)]** をクリックまたはタップすると、自動的にアプリが生成されます。
   
    この時点で、クイック ツアーの開始を求められる場合があります。 クイック ツアーは後からいつでも開始できます。右上隅の疑問符をクリックまたはタップし、**[Take the intro tour]** (クイック ツアーの開始) をクリックまたはタップしてください。
6. 左側のナビゲーション バーで、右上のアイコンをクリックまたはタップしてサムネイル表示に切り替えます。
   
    ![表示の切り替え](./media/data-platform-create-app/toggle-view.png)

## <a name="customize-the-browse-screen"></a>ブラウズ画面のカスタマイズ
1. 右側のウィンドウで、見出しのみを表示するレイアウトをクリックまたはタップします。
   
    ![レイアウトを選択する](./media/data-platform-create-app/choose-gallery-layout.png)
2. 検索ボックスの下の**ラベル** コントロールをクリックまたはタップして選択します。
   
    ![ラベルの選択](./media/data-platform-create-app/select-textbox.png)
3. 右側のウィンドウで、ドロップダウン リストから **[Surname of Given name]** (姓) を選択します。
   
     選択した**ラベル** コントロールに、そのフィールドのデータが表示されます。
4. ブラウズ画面で、1 つ目を除く任意の名前をクリックまたはタップしてギャラリーを選択します。
   
    ギャラリーの周囲に選択ボックスが表示されます。
   
    ![ギャラリーを選択する](./media/data-platform-create-app/select-gallery.png)
5. 次の式を選択し、Ctrl + C キーを押してコピーします。
   
    **SortByColumns(Search(Contact, TextSearchBox1.Text, "Name_Surname"), "Name_Surname", If(SortDescending1, Descending, Ascending))**
6. 左上隅のプロパティ一覧に **Items** が表示されていることを確認します。
7. 数式バーで既定の式を選択します。
   
    ![Items プロパティの既定値](./media/data-platform-create-app/default-items.png)
8. Del キーを押して既定の式を削除し、コピーした式を貼り付けます。 ギャラリーに表示される名前がアルファベット順に並べ替えられます。

## <a name="test-the-browse-screen"></a>ブラウズ画面のテスト
1. F5 キーを押すか、右上隅の**再生**ボタンをクリックまたはタップして、プレビュー モードを開始します。
2. タッチ スクリーンを使用するか、マウスホイールを使用するか、またはギャラリーをマウスでポイントしてスクロール バーを表示し、スクロール操作で最初から最後までレコードを表示します。
3. 右上隅にある並べ替えボタンをクリックまたはタップして名前の表示順を変更します。
   
    ![並べ替え順を変更する](./media/data-platform-create-app/sort-button.png)
4. 検索ボックスに文字を入力すると、その文字を含む名前のみが表示されます。
5. 検索ボックスからすべてのテキストを削除して、一覧の最初の名前の右側にある矢印をクリックまたはタップします。
   
    詳細画面が開き、選択した連絡先の詳細が表示されます。
6. Esc キーを押すか、右上隅のタイトル バーの下にある**閉じる**ボタンをクリックまたはタップして、デザイン ワークスペースに戻ります。

## <a name="customize-the-other-screens"></a>他の画面をカスタマイズする
1. **DetailScreen** が表示されていない場合は、左側のナビゲーション バーで中央のサムネイルをクリックまたはタップします。
2. **DetailScreen** の上部にある**[氏名]** をクリックまたはタップして、その画面のフォームをカスタマイズするオプションを表示します。
3. 右側のウィンドウで **[Name_MiddleName]** の目のボタンをクリックまたはタップして、フィールドを非表示にします。
4. 右側のウィンドウで **[Name_Surname]** の目のボタンをクリックまたはタップして、フィールドを表示します。
5. 右側のウィンドウで **[Name_Surname]** を上方向にドラッグし、**[Name_GivenName]** の下にドロップします。
   
    **DetailScreen** に変更内容が反映されます。
6. 左側のナビゲーション バーで、下のサムネイルをクリックまたはタップして **EditScreen** を表示し、**EditScreen** と **DetailScreen** が一致するまで前の手順を繰り返します。

## <a name="test-the-app"></a>アプリケーションをテストする
1. 左側のナビゲーション バーで一番上のサムネイル画像をクリックまたはタップし、ブラウズ画面を開きます。
2. F5 キーを押すか、右上隅の**再生**ボタンをクリックまたはタップして、プレビュー モードを開始します。
3. ブラウズ画面の右上隅にあるプラス記号のボタン (**+**) をクリックまたはタップしてレコードを作成します。
4. **[名]** と **[姓]** フィールドにテキストを追加し、チェック マーク ボタンをクリックまたはタップして新しいレコードを保存し、ブラウズ画面に戻ります。
5. 先ほど作成したレコードを検索し、右側にある矢印をクリックまたはタップして、詳細画面でレコードを表示します。
6. 右上隅にある鉛筆ボタンをクリックまたはタップして、編集画面でレコードを表示します。
7. **[名]** フィールドのデータを変更し、チェック マーク ボタンをクリックまたはタップして変更を保存します。
8. 作成および更新したレコードを右上隅にあるごみ箱ボタンをクリックまたはタップして削除します。

## <a name="next-steps"></a>次の手順
[Common Data Service データベースを使用してアプリを最初から作成する](data-platform-create-app-scratch.md)

