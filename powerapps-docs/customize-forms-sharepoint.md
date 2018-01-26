---
title: "フォームのカスタマイズ | Microsoft Docs"
description: "どのデータを、どのような順番で、どのコントロールに表示するかを指定します。"
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
ms.date: 10/16/2016
ms.author: sharik
ms.openlocfilehash: 51b784376834d8eaa5d186ad0d517e20cf088f38
ms.sourcegitcommit: 6afca7cb4234d3a60111c5950e7855106ff97e56
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2018
---
# <a name="customize-forms-in-powerapps"></a>PowerApps でのフォームのカスタマイズ
ユーザーにとって見やすく更新しやすいコントロールに、最も重要なデータを、直感的に伝わりやすい順序で表示するように、**表示フォーム** コントロールと**編集フォーム** コントロールをカスタマイズします。

それぞれのフォームは、少なくとも 1 つのカードで構成され、データ ソースから取得された特定の列のデータが個々のカードに表示されます。 このトピックの手順に従うことで、フォームに表示するカードを指定したり、フォーム内でカードの位置を上げ下げしたり、それぞれの列から取得したデータをカード内に表示するときの体裁を設定したりすることができます。

PowerApps の基本的な事柄については、「[PowerApps の概要](getting-started.md)」を参照してください。

## <a name="prerequisites"></a>前提条件
このチュートリアルは、概念全般を理解する目的でのみご覧いただいても、目的を果たすために各手順を忠実に実行していただいてもかまいません。

1. PowerApps から SharePoint への[接続を作成](connect-to-sharepoint.md)します。

2. SharePoint リストを作成します ([レイアウトのカスタマイズ](customize-layout-sharepoint.md)についてのページを参照)。

3. そのリストに基づいて[アプリを自動的に生成](app-from-sharepoint.md)します。

4. 左側のナビゲーション バーで、右上のアイコンをクリックまたはタップしてサムネイル表示に切り替えます。

    ![表示の切り替え](./media/customize-forms-sharepoint/toggle-view.png)

## <a name="show-and-hide-cards"></a>カードの表示と非表示
1. 左側のナビゲーション バーで中央のサムネイルをクリックまたはタップし、**DetailsScreen1** を選択します。

    ![詳細画面を選択](./media/customize-forms-sharepoint/details-thumbnail.png)

2. いずれかのカードをクリックまたはタップして選択し、フォームのカスタマイズ オプションを右側のペインに表示します。

    ![カードを選択](./media/customize-forms-sharepoint/select-card.png)

3. 右側のウィンドウで、**AccountID** カードについては、チェックボックスをクリックまたはタップして非表示状態に、**ID** 列については、チェックボックスをクリックまたはタップして表示状態にします。

    ![カードを表示](./media/customize-forms-sharepoint/checkbox.png)

## <a name="reorder-the-cards"></a>カードの並べ替え
* **Title** カードをクリックまたはタップして選択し、そのタイトル バーを、**OrderDate** カードが強調表示されるまで上へドラッグします。

    ![カードの移動](./media/customize-forms-sharepoint/move-card.png)

    マウス ボタンから手を離すと、移動中のカードは、強調表示されているカードのすぐ上に表示されます。

    ![並べ替え後のカード](./media/customize-forms-sharepoint/reordered-card.png)

## <a name="run-the-app"></a>アプリの実行
1. 左側のナビゲーション バーで一番上のサムネイルをクリックまたはタップし、**BrowseScreen1** を選択します。

    ![BrowseScreen1 のサムネイル](./media/customize-forms-sharepoint/browse-thumbnail.png)

2. F5 キーを押して (または右上隅の**プレビュー** アイコンをクリックして) プレビュー モードを開きます。  

    ![プレビュー アイコン](./media/customize-forms-sharepoint/open-preview.png)

3. 右上隅のプラス アイコンをクリックまたはタップして、**EditScreen1** でレコードを追加します。

    ![レコードを追加](./media/customize-forms-sharepoint/add-record.png)

4. 必要なデータを追加し、右上隅のチェックマーク アイコンをクリックまたはタップして、新しいレコードを SharePoint リストに保存し、**BrowseScreen1** に戻ります。

    ![レコードの保存](./media/customize-forms-sharepoint/save-record.png)

5. 今作成した項目の矢印をクリックまたはタップして、その詳細を **DetailScreen1** に表示します。  

    ![右矢印](./media/customize-forms-sharepoint/right-arrow.png)

6. 右上隅の編集アイコンをクリックまたはタップして、**EditScreen1** でレコードを更新します。

    ![レコードを編集](./media/customize-forms-sharepoint/edit-record.png)

7. 少なくとも 1 つのフィールドの情報を変更し、右上隅のチェック マークをクリックまたはタップして SharePoint リストに変更内容を保存し、**DetailScreen1** に戻ります。  

    ![変更を保存](./media/customize-forms-sharepoint/save-record.png)

8. 右上隅にあるごみ箱アイコンをクリックまたはタップして、先ほど更新したレコードを削除し、**BrowseScreen1** に戻ります。

    ![レコードを削除](./media/customize-forms-sharepoint/delete-record.png)

9. Esc キーを押して (または、PowerApps のタイトル バーの "*下*" の左上隅にある閉じるアイコンをクリックまたはタップして)、プレビュー モードを終了します。

    ![プレビュー モードの終了](./media/customize-forms-sharepoint/close-preview.png)

## <a name="next-steps"></a>次の手順
* 他のデバイスから実行できるように、Ctrl + S キーを押してアプリを保存する。
* 他のユーザーが実行できるように[アプリを共有](share-app.md)する。
