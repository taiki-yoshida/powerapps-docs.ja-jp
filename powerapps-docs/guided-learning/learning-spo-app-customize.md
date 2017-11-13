---
title: "アプリのカスタマイズ (SharePoint リスト) | Microsoft Docs"
description: "アプリの画面、コントロール、およびフィールドを更新します"
services: 
suite: powerapps
documentationcenter: na
author: mgblythe
manager: anneta
editor: 
tags: 
featuredvideoid: KydeusvKndQ
courseduration: 5m
ms.service: powerapps
ms.devlang: na
ms.topic: get-started-article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 12/09/2016
ms.author: mblythe
ms.openlocfilehash: 8aa1db7735416a9dc59fc2c726c5b506fd438a03
ms.sourcegitcommit: 43be6a4e08849d522aabb6f767a81c092419babc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2017
---
# <a name="customize-the-app-sharepoint-list"></a>アプリのカスタマイズ (SharePoint リスト)
このセクションの最初の 2 つのトピックで、SharePoint リストからアプリを生成し、生成したアプリを詳しく確認して 3 画面アプリの構造について学習しました。 PowerApps に生成されるアプリは便利ですが、多くの場合は、生成された後でアプリをカスタマイズします。 このトピックでは、アプリの各画面の基本的な変更点の概要を説明します。 他にもアプリをカスタマイズする方法はたくさんありますが、それらについては後のトピックで説明します。 ひとまずはこのトピックの内容を理解し、足掛かりとしてください。 リスト、Excel ファイル、またはその他のソースから生成した任意のアプリを取り上げ、カスタマイズ方法を確認しましょう。 これが本当にアプリの構造を学習するベストな方法なのです。

## <a name="browse-screen"></a>ブラウズ画面
ブラウズ画面からはじめます。 SharePoint リストには、各製品のイメージが含まれていますが、既定ではイメージは表示されません。 これを修正しましょう。 右側のウィンドウの **[Layout]** (レイアウト) タブで、ブラウズ画面とは異なるレイアウトを選択します。 変更と同時に PowerApps がアプリを更新するので、結果はすぐに表示されます。

![ブラウズ画面のレイアウトを変更する](./media/learning-spo-app-customize/generate-change-layout.png)

右の基本レイアウトを使用して、表示されるフィールドを変更しましょう。 最初の項目のフィールドをクリックまたはタップして、右側のウィンドウで項目ごとに表示されるデータを変更します。 これにより、リストの各項目の概要が分かりやすくなります。

![ブラウズ画面のフィールドを変更する](./media/learning-spo-app-customize/generate-browse-fields.png)

## <a name="details-screen"></a>詳細画面
詳細画面では、フィールドの順序を変更し、イメージも表示してみます。 この画面にはさまざまなコントロールがあるため、プロセスは参照画面とは少し異なります。 フィールドをクリックまたはタップして、右側のウィンドウで、**[Title]** (タイトル) フィールドを一番上にドラッグします。 次に、**[Image]** (イメージ) フィールドをクリックまたはタップして、表示します。

![詳細画面のフィールドを変更する](./media/learning-spo-app-customize/generate-detail-fields.png)

## <a name="editcreate-screen"></a>編集/作成画面
最後に、エントリを編集したり作成したりする画面で、テキストを入力しやすいようにフィールドを変更してみます。 **[概要]** フィールドのドロップダウン リストをクリックまたはタップして、**複数行テキストの編集**コントロールをクリックまたはタップします。

![編集画面のフィールドを変更する](./media/learning-spo-app-customize/generate-edit-fields.png)

いくつかの基本的な手順で、生成されたアプリの使い勝手と外観をどれほど改善できるかが分かりました。 このトピックでは、PowerApps Studio の UI に重点を置きました。PowerApps Studio の UI にはアプリをカスタマイズするための多くのオプションがあることがわかりました。 次のトピックでは、数式について説明します。数式は、アプリを動作させるうえで重要な役割を果たします。  

