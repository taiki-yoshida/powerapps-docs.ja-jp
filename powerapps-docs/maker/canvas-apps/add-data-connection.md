---
title: アプリへのデータ接続の追加 | Microsoft Docs
description: 既存のアプリや空のアプリにデータ接続を追加できます
services: ''
suite: powerapps
documentationcenter: na
author: archnair
manager: anneta
editor: ''
tags: ''
ms.service: powerapps
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/02/2017
ms.author: archanan
ms.openlocfilehash: 2134aa28f1b842614e1f4b82acaca2f100126120
ms.sourcegitcommit: 59785e9e82da8f5bd459dcb5da3d5c18064b0899
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/22/2018
---
# <a name="add-a-data-connection-in-powerapps"></a>PowerApps でデータ接続を追加する
PowerApps で、既存のアプリまたはゼロから作成するアプリにデータ接続を追加します。 このトピックでは PowerApps Studio を使用しますが、[接続管理](add-manage-connections.md)トピックで説明しているように、[powerapps.com](https://web.powerapps.com) を利用することもできます。

アプリのデータ接続は、SharePoint、Salesforce、OneDrive、または[他の多くのデータ ソースのいずれか](connections-list.md)に接続できます。

この記事の後に来る[次のステップ](#next-steps)は、以下に示す例のように、接続したデータ ソースのデータをアプリで表示および管理することです。

* OneDrive に接続し、アプリ内で Excel ブックのデータを管理する。
* Twilio に接続し、アプリから SMS メッセージを送信する。
* SQL Server に接続し、アプリからテーブルを更新する。

## <a name="prerequisites"></a>前提条件
PowerApps に[サインアップ](../signup-for-powerapps.md)し、[インストール](http://aka.ms/powerappsinstall)して開きます。その後、サインアップに使用したのと同じ資格情報を入力してサインインします。

## <a name="background-on-data-connections"></a>データ接続の背景
ほとんどの PowerApps アプリでは、クラウド サービスに格納されている**データ ソース**と呼ばれる外部情報を使用します。 一般的な例は、OneDrive for Business に格納されている Excel ファイル内のテーブルです。 これらのデータ ソースには、アプリから**コネクタ**を使用してアクセスできます。

最も一般的なデータ ソースはテーブルで、情報の取得と保存に使用できます。 データ ソースへのコネクタを使用すれば、Microsoft Excel ブック、SharePoint リスト、SQL テーブル、その他多くの形式でデータの読み書きを行えます。それらのデータは、OneDrive for Business、DropBox、SQL Server などのクラウド サービスに格納できます。

テーブル以外のデータ ソースとして、電子メール、予定表、Twitter、通知があります。

**[ギャラリー](controls/control-gallery.md)**、**[表示フォーム](controls/control-form-detail.md)**、**[編集フォーム](controls/control-form-detail.md)** コントロールを使用すると、データ ソースからデータを読み書きするアプリを簡単に作成できます。 最初に、[データ フォームについて](working-with-forms.md)の記事をご覧ください。

## <a name="add-a-connection"></a>接続を追加する
1. 画面の左端にある **[ファイル]** メニューの **[新規]** をクリックまたはタップします。

    ![[ファイル] メニューの [新規] オプション](./media/add-data-connection/file-new.png)

2. **[空のアプリ]** タイルで、**[携帯電話レイアウト]** をクリックまたはタップします。

    ![アプリを最初から作成する](./media/add-data-connection/blank-app.png)

3. 中央のウィンドウで、**[データに接続]** をクリックまたはタップします。

4. 使用する接続が **[データ]** ウィンドウの接続の一覧に表示されている場合は、その接続をクリックまたはタップしてアプリに追加します。 それ以外の場合、次のステップに進んでください。

    ![データ ソースの追加](./media/add-data-connection/choose-existing-connections.png)

5. **[新しい接続]** をクリックまたはタップして、コネクタの一覧を表示します。

    ![接続の追加](./media/add-data-connection/new-connection.png)

6. 作成する接続の種類 (たとえば、**Office 365 Outlook**) が表示されるまでコネクタの一覧をスクロールし、それをクリックまたはタップします。

    ![接続の選択](./media/add-data-connection/choose-connection.png)

7. **[作成]** をクリックまたはタップして、接続の作成とアプリへの追加の両方を行います。

    **Microsoft Translator** などのコネクタでは、追加の手順を実行しなくても、すぐにデータを表示できます。 コネクタによっては、資格情報の入力や、特定のデータ セットの指定などの手順が要求されることがあります。 たとえば、[SharePoint](connections/connection-sharepoint-online.md) と [SQL Server](connections/connection-azure-sqldatabase.md) では、使用する前に追加情報の入力を求められます。

## <a name="view-or-change-a-data-source"></a>データ ソースの表示または変更
アプリを更新する際、ギャラリー、フォーム、または **Item** プロパティを持つ別のコントロールに表示されるデータ ソースを特定または変更する必要があることがあります。 たとえば、他の人が作成したアプリを操作している場合や、自分が以前構成したデータ ソースを再度確認する場合などです。

1. データ ソースを特定するコントロールを選択します。

    たとえば、左端付近にある画面およびコントロールの階層一覧内のギャラリーをクリックまたはタップして、(ギャラリー内のコントロールではなく) ギャラリーを選択します。

    右側のウィンドウの **[プロパティ]** タブにデータ ソース名が表示されます。

    ![[プロパティ] タブ上のデータ ソース](./media/add-data-connection/properties-tab.png)

2. データ ソースの詳細を表示または変更するには、右側のウィンドウで **[データ]** をクリックまたはタップします。

    ![データ ウィンドウ](./media/add-data-connection/data-pane.png)

3. データ ソースを変更するには、データ ソースの横にある下矢印をクリックまたはタップして、別のソースを選択または作成します。

## <a name="next-steps"></a>次の手順
* Excel、SharePoint、SQL Server などのソースにあるデータを表示および更新するには、[ギャラリーを追加](add-gallery.md)して、[フォームを追加](add-form.md)します。
* [Office 365 Outlook](connections/connection-office365-outlook.md)、[Twitter](connections/connection-twitter.md)、[Microsoft Translator](connections/connection-microsoft-translator.md) などのソースの場合は、各コネクタに用意された機能を使用して表示や更新を行います。
