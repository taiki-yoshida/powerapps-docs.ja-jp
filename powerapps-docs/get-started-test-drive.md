---
title: "テンプレートからアプリを作成する | Microsoft Docs"
description: "テンプレートから自動的にアプリを作成して保存する手順について説明します。"
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
ms.date: 04/03/2017
ms.author: karthikb
ms.openlocfilehash: 17214cf93b22973198b7d801ae95d159ef467d38
ms.sourcegitcommit: 43be6a4e08849d522aabb6f767a81c092419babc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2017
---
# <a name="create-and-run-an-app-from-a-template"></a>テンプレートからアプリを作成して実行する
特定の用途のテンプレートから自動的にアプリを作成して実行し、その既定の動作を見てみましょう。 アプリをカスタマイズして保存し、他のユーザーと共有する方法を体験します。

**前提条件**

* PowerApps に[サインアップ](signup-for-powerapps.md)し、[インストール](http://aka.ms/powerappsinstall)して開きます。その後、サインアップに使用したのと同じ資格情報を入力してサインインします。
  
    **注**: この機能を使用するには、バージョン 2.0.510 以降が実行されている必要があります。 ご使用のバージョンを確認するには、左側に表示される **[File (ファイル)]** メニューの **[Account (アカウント)]** をクリックまたはタップし、**[Product information (製品情報)]** の下を見てください。
* クラウド ストレージ アカウント (DropBox、OneDrive、Google Drive など)。

## <a name="create-an-app"></a>アプリを作成する
1. Windows 用 PowerApps Studio または Web 用の PowerApps Studio で、**[新規]** (画面の左端近く) をクリックまたはタップします。
   
    ![[File (ファイル)] メニューの [New (新規)] オプション](./media/get-started-test-drive/file-new.png)
2. **アプリ テンプレート** タイルで、**[携帯電話レイアウト]** をクリックまたはタップします。
   
   **注:** タブレット用レイアウトのテンプレートからアプリを作成することもできますが、このチュートリアルでは、主にスマートフォン用のオプションについて説明します。
   
   ![タブレット用またはスマートフォン用にアプリを作成するためのオプション](./media/get-started-test-drive/phone-app.png)
   
   テンプレートの一覧が表示されます。
3. クラウド ストレージ アカウントへの接続がない場合は、次の作業を行います。
   
   1. 画面の下部に表示される **[選択]** をクリックまたはタップします。
      
       ![テンプレート ビュー内で接続を作成するためのオプション](./media/get-started-test-drive/add-connection.png)
   2. 使用するアカウントをタップまたはクリックします。
      
       ![テンプレートからアプリを作成するための接続の一覧](./media/get-started-test-drive/store-data.png)
   3. 資格情報を入力し、**[使用]** をクリックまたはタップしてアクセスを許可します。
      
       指定した接続が画面の下部に表示されます。
4. テンプレートの一覧で、いずれかのテンプレートをクリックまたはタップし、右下隅にある **[Use (使用)]** をクリックまたはタップします。
   
    ![PowerApps テンプレートを開く](./media/get-started-test-drive/open-template.png)
   
    サンプル データがクラウド ストレージ アカウントにコピーされ、アプリが作成されて、そのホーム ページが表示されます。

## <a name="run-the-app"></a>アプリの実行
テンプレートから作成されたアプリが既定のワークスペースに表示されます。カスタマイズに伴うほとんどの作業は、このワークスペースで行うことになります。 アプリに変更を加える前に、このセクションの手順に従い、**プレビュー** モードでアプリの動作を詳しく見てみましょう。

**ヒント:** アプリの設計と開発は既定のワークスペースで行いますが、実際に他のユーザーに配布する前のテストは**プレビュー** モードで行います。

1. まだ PowerApps を使ったことがない方は、クイック ツアーに進んでください (不要であれば **[Skip (スキップ)]** をクリックまたはタップしてください)。
   
    ![クイック ツアーの開始画面](./media/get-started-test-drive/quick-tour.png)
   
    クイック ツアーは後からいつでも開始できます。右上隅の疑問符アイコンをクリックまたはタップし、**[Take the intro tour (クイック ツアーの開始)]** をクリックまたはタップしてください。
2. 左側のナビゲーション バーで一番上の方にある画面をクリックまたはタップします。
3. F5 キーを押して (または、右上隅にある右矢印をクリックまたはタップして)、**プレビュー** モードでアプリを開きます。
   
    ![プレビュー モードを開始するためのボタン](./media/get-started-test-drive/open-preview.png)
   
    アプリには、その機能を紹介するためのサンプル データがあらかじめ追加されています。 たとえば、Cost Estimator アプリには、予定を作成するためのデータのほか、特定の大きさの部屋に特定の床材を設置する際にかかるコストを見積もるためのサンプル データが含まれています。
4. アプリの既定の動作をよく観察し、行った変更がクラウド アカウントのデータに正しく反映されることを確認します。
   
    たとえば、Cost Estimator アプリで人と会う予定を作成したり、コストの見積もりを作成したりします。
5. 右上隅の (PowerApps タイトル バーの下にある) **"X"** アイコンを選択して既定のワークスペースに戻ります。
   
    ![プレビュー モードを終了するためのボタン](./media/get-started-test-drive/close-preview.png)

## <a name="customize-the-app"></a>アプリのカスタマイズ
このアプリを含め、すべてのアプリはカスタマイズすることができます。次に示したのは、主なカスタマイズの例です。

* [画面のサイズや方向、またはその両方を変更する](set-aspect-ratio-portrait-landscape.md)
* [別のデータ ソースを追加する](add-data-connection.md)
* [1 つ以上の画面を追加する](add-screen-context-variables.md)
* [他のコントロールを追加して構成する](add-configure-controls.md)
* [アプリの動作を変更する](working-with-formulas.md)

## <a name="next-steps"></a>次の手順
1. Ctrl + S キーを押してアプリに名前を付けたら、**[Save (保存)]** をクリックまたはタップしてクラウドにアプリを保存します。
2. 組織内の他のユーザーと[アプリを共有](share-app.md)します。
   
    **注**: アプリを共有する前に、その相手となるユーザーがデータを利用できる状態になっていることを確認してください。 たとえば、クラウド ストレージ アカウント内の [Excel ファイルやその他のファイルを共有](share-app-data.md)する必要があります。

