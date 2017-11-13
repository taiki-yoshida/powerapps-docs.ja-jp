---
title: "Web ブラウザーでのアプリの使用 | Microsoft Docs"
description: "Web ブラウザーでアプリを使用する方法のチュートリアル"
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
ms.date: 10/12/2017
ms.author: litran
ms.openlocfilehash: 1cdd7fbf5b5940550e6e7c98ecaf2262940baa1c
ms.sourcegitcommit: 43be6a4e08849d522aabb6f767a81c092419babc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2017
---
# <a name="use-powerapps-in-a-web-browser"></a>Web ブラウザーでの PowerApps の使用
PowerApps でアプリを作成すると、そのアプリをブラウザーで実行できます。これには、[Dynamics 365](https://home.dynamics.com) を開き、ホーム ページでアプリのタイルをクリックするかタップします。

**注**: [Microsoft Dynamics 365](https://docs.microsoft.com/en-us/dynamics365/) に関する全般的な情報を参照するか、Sales などの Dynamics 365 アプリについて質問がある場合は[サポートにお問い合わせ](https://www.microsoft.com/en-us/dynamics365/contact-us)ください。

サポートされているブラウザーとオペレーティング システムは次のとおりです。

| **ブラウザー** | **オペレーティング システム** |
| --- | --- |
| Google Chrome (最新バージョン) |Windows 7 SP1、8.1、および 10 <br>macOS <br>iOS 8 以降<br>Android |
| Microsoft Edge |Windows 10 |
| Microsoft Internet Explorer 11 (互換表示オフ) |Windows 7 SP1、8.1、および 10 |
| Mozilla Firefox (最新バージョン) |Windows 7 SP1、8.1、および 10 <br> Android <br>macOS |
| Apple Safari (最新バージョン) |macOS <br> iOS 8 以降 |

アプリで使用されているコントロールにブラウザーでサポートされていないものがある場合は、iOS、Android、または Windows 用 PowerApps Mobile をダウンロードし、モバイル デバイス (スマートフォンなど) でそのアプリを使用してください。

## <a name="find-an-app-on-the-home-page"></a>ホーム ページでアプリを探す
ホーム ページには、複数の種類のビジネス アプリが表示される場合がありますが、検索ボックスにアプリ名の一部を入力すると特定のアプリを見つけることができます。 また、PowerApps で作成されたアプリのみを表示するように一覧をフィルター処理することもできます。

最近インストールしたアプリは、アプリの一覧にすぐに表示されない場合があります。 すべてのアプリを表示するには **[同期]** をクリックまたはタップしてください。ただし、この処理には最大 1 分かかる場合があります。

![](./media/run-app-browser/dynamics-365-home.png)

## <a name="open-an-app-from-the-task-pane"></a>作業ウィンドウからアプリを開く
アプリが見つかったら、より簡単にアクセスできるように、そのアプリを作業ウィンドウにピン留めすることができます。 アプリをピン留めするには、アプリ タイルの省略記号 (...) をクリックまたはタップし、**[Pin this app] /(このアプリをピン留め/)** をクリックまたはタップします。

![](./media/run-app-browser/homepage-pin.png)

その後、アプリは作業ウィンドウの**マイ アプリ**に表示されます。この作業ウィンドウを開くには、左上隅の **[Dynamics 365]** をクリックまたはタップします。

![](./media/run-app-browser/taskpane.png)

## <a name="open-an-app-from-a-url"></a>URL からアプリを開く
アプリの URL は、ブラウザーのブックマークとして保存することも、電子メールでリンクとして送信することもできます。 他のユーザーが PowerApps でアプリを作成し、自分と共有した場合、受信した電子メールに記載されているリンクをクリックまたはタップしてそのアプリを実行できます。 いずれの場合も、Azure Active Directory の資格情報を使用してサインインするように求められることがあります。

![](./media/run-app-browser/web-login.png)

## <a name="connect-to-data"></a>データに接続する
アプリがデータ ソースへの接続を必要とする場合、またはデバイスの機能を使用するための同意を必要とする場合、アプリを使用する前に確認が求められます。  

![接続](./media/run-app-browser/app-connection.png)

通常、このことが求められるのは初回のみです。

## <a name="close-an-app"></a>アプリを閉じる
アプリを閉じるには、Dynamics 365 ホーム ページからサインアウトするか、別のアプリを開きます。

