---
title: アプリを保存して発行する | Microsoft Docs
description: アプリ メーカー向けのアプリを保存および発行するための手順
services: ''
suite: powerapps
documentationcenter: na
author: SKjerland
manager: anneta
editor: ''
tags: ''
ms.service: powerapps
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 09/14/2017
ms.author: sharik
ms.openlocfilehash: 739813b2b4905653543461008986901d4e2ee95b
ms.sourcegitcommit: 59785e9e82da8f5bd459dcb5da3d5c18064b0899
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/22/2018
---
# <a name="save-and-publish-an-app-in-powerapps"></a>PowerApps でアプリを保存して発行する
アプリへの変更を保存すると、自分とアプリを編集するアクセス許可を持つ他のユーザーのみに、自動的にアプリが発行されます。 変更が完了したら、アプリを共有しているすべてのユーザーが利用できるように、明示的に発行する必要があります。

アプリを共有する方法については、「[PowerApps でのアプリの共有](share-app.md)」を参照してください。

## <a name="save-changes-to-an-app"></a>アプリへの変更を保存する
PowerApps Studio で、**[ファイル]** メニュー (左端) で **[保存]** をクリックまたはタップして、次のいずれかの手順に従います。

* アプリを以前に保存していない場合は、アプリの名前を指定して、**[保存]** をクリックまたはタップします。

    ![新しいアプリを保存する](./media/save-publish-app/save-as.png)
* アプリを保存したことがある場合は、**[保存]** をクリックまたはタップします。  

    ![更新したアプリを保存する](./media/save-publish-app/save-app.png)

また、PowerApps では、2 分ごとにアプリを定期的に保存できます。 アプリをいったん保存すると、PowerApps はユーザーが [保存] アクションを押したりタップしたりしなくても、アプリのバージョンを定期的に保存し続けます。 作成者は **[ファイル]** メニューの **[アカウント]** タブで**自動保存**設定を有効または無効にできます。

![自動保存設定](./media/save-publish-app/autosave.png)

## <a name="publish-an-app"></a>アプリを公開します。
1. PowerApps Studio で、**[ファイル]** メニュー (左端) で **[保存]** をクリックまたはタップして、**[このバージョンの発行]** をクリックまたはタップします。

    ![アプリを発行する](./media/save-publish-app/publish-app.png)
2. **[発行]** ダイアログ ボックスで、**[このバージョンの発行]** をタップまたはクリックして、アプリを共有しているすべてのユーザーにアプリを発行します。

   ![発行を確認する](./media/save-publish-app/publish-review.png)

   > [!NOTE]
> アプリを PowerApps の最新のバージョンと同期させておくために、最後に公開した日から 6 か月以内にアプリを更新または再発行することをお勧めします。 6 か月以内に更新または再発行がされない場合、警告なしにアプリが動作を停止することがあります。

## <a name="identify-the-live-version"></a>ライブ バージョンを指定する
[powerapps.com](https://web.powerapps.com) では、**[ファイル]** メニュー (左端) の **[アプリ]** をクリックまたはタップし、アプリの詳細アイコンをクリックまたはタップして、**[バージョン]** タブをクリックまたはタップします。

**ライブ** バージョンは、アプリを共有しているすべてのユーザーに発行されます。 アプリの最新バージョンは、編集のアクセス許可を持つユーザーのみが入手できます。

![ポータルから発行する](./media/save-publish-app/publish-portal.png)

最新バージョンを発行するには、**[このバージョンの発行]** をクリックまたはタップして、**[発行]** ダイアログ ボックスの **[このバージョンの発行]** をクリックまたはタップします。

## <a name="next-steps"></a>次の手順
* powerapps.com から[アプリの名前を変更します](set-name-tile.md)。
* アプリに複数のバージョンがある場合、[アプリを復元します](restore-an-app.md)。
