---
title: "スマートフォンまたはタブレットで PowerApps を使用する | Microsoft Docs"
description: "スマートフォンまたはタブレットでの PowerApps の使用に関するチュートリアル"
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
ms.date: 01/16/2018
ms.author: sharik
ms.openlocfilehash: e6d0ae8e2a00769a6abe1428e2756159bbbf9086
ms.sourcegitcommit: 6afca7cb4234d3a60111c5950e7855106ff97e56
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2018
---
# <a name="use-powerapps-on-a-phone-or-a-tablet"></a>スマートフォンまたはタブレットで PowerApps を使用する
PowerApps を使用して構築したアプリは、Windows、iOS、Android、または Web ブラウザーで実行できます。 モバイル デバイスで実行されるアプリでは、位置情報やカメラなどのデバイス機能を活用できます。 PowerApps は、Windows ストア、App Store、または Google Play からダウンロードできます。

## <a name="prerequisites"></a>前提条件
* 次のいずれかが必要です。
  * 自分が[テンプレート](get-started-test-drive.md)、[データ](get-started-create-from-data.md)、または[空のキャンバス](get-started-create-from-blank.md)から構築したアプリ。
  * 他のユーザーが構築し、自分にユーザー アクセス許可が与えられて、共有されているアプリ。
* iPhone、iPad、または Android デバイスにインストールされた PowerApps。 サポートされている特定のバージョンを次に示します。  
  * iOS 9.3 以降 (推奨: iOS 10 以降で少なくとも 2 GB の RAM を搭載していること)
  * Android 5 以降 (推奨: Android 7 以降で少なくとも 4 GB の RAM を搭載していること)

PowerApps の基本的な事柄については、「[PowerApps の概要](getting-started.md)」を参照してください。

## <a name="sign-in-to-powerapps"></a>PowerApps へのサインイン
初めて PowerApps を開くと、Azure Active Directory の資格情報を使用してサインインすることを求められます。  

![ユーザーのログイン](./media/run-app-client/run-client-login.png)

## <a name="app-filters-and-sorting-options"></a>アプリのフィルターと並べ替えのオプション
次のカテゴリのいずれかを検索すると、アプリをすばやく見つけることができます。

* **すべて**: 自分が作成したアプリ、他のユーザーが共有したアプリなど、アクセスできるすべてのアプリ。
* **マイ アプリ**: 少なくとも 1 回実行したアプリ。
* **サンプル**: 架空のデータにより実際のアプリケーション シナリオを紹介し、設計の可能性を調査できるようにする、Microsoft が提供したサンプルのアプリ。
* **お気に入り**: 各アプリの "…" オプションを使用してマークしたアプリ。 アプリのマークを解除して、このリストから削除できます。

    ![アプリのフィルター](./media/run-app-client/run-client-applist.png)

リストを選択したら、アプリを前回開いた日付または変更した日付によって、リストを並べ替えることもできます。 PowerApps を閉じて再起動したときも、これらの設定は保持されます。  

## <a name="open-an-app"></a>アプリを開く
タブレットまたはスマートフォンでアプリを開くには、アプリのアイコンをタップするか、他のユーザーが自分とアプリを共有しているときに表示されるプッシュ通知をタップします。

PowerApps を初めて使用する場合は、画面に PowerApps を終了するためのスワイプ ジェスチャが表示されます。

![アプリの起動](./media/run-app-client/run-client-app.png)

## <a name="give-consent"></a>同意
アプリでデータ ソースへの接続が必要か、デバイスの機能を使用するための同意が必要な場合は、アプリを使用する前に接続を確認するか、同意する必要があります。  

![接続](./media/run-app-client/app-connection.png)

通常、このことが求められるのは初回のみです。

## <a name="exit-the-app"></a>アプリの終了
* Android デバイスでは、右へスライドします (または [戻る] ボタンを押してから、アプリを終了することを確認します)。
* iOS デバイスでは、右へスライドします。

## <a name="share-the-app"></a>アプリの共有
[powerapps.com](https://web.powerapps.com) からアプリを共有する方法については、「[Sharing an app (アプリの共有)](share-app.md)」を参照してください。

## <a name="pin-an-app-to-the-home-screen"></a>ホーム画面へのアプリのピン留め
アプリをダウンロードして 1 回以上使用した場合に、アプリをデバイスのホーム画面にピン留めしてすばやくアクセスできます。 アプリの省略記号 (...) をタップして、**[ピン留め]** をタップし、表示される指示に従います。

![アプリのピン留め](./media/run-app-client/run-client-pin.png)
