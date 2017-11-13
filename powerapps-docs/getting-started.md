---
title: "概要 | Microsoft Docs"
description: "Microsoft PowerApps で手軽にカスタム ビジネス アプリを作成して使用する方法"
services: 
suite: powerapps
documentationcenter: na
author: skjerland
manager: anneta
editor: 
tags: 
ms.service: powerapps
ms.devlang: na
ms.topic: hero-article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/28/2017
ms.author: sharik
ms.openlocfilehash: 43f912885a70d2b86713c5b4ffc5043d1401a1fa
ms.sourcegitcommit: 43be6a4e08849d522aabb6f767a81c092419babc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2017
---
# <a name="introduction-to-powerapps"></a>PowerApps の概要
PowerApps に興味を持っていただきありがとうございます。 PowerApps では、自分で作成したアプリ、または別のユーザーが作成し共有したアプリを実行して、組織のデータを管理できます。 アプリは**[携帯電話などのモバイル デバイス](run-app-client.md)**か、Dynamics 365 を開いて**[ブラウザーで](run-app-browser.md)**実行できます。 C# などのプログラミング言語をまったく学習することなく、あらゆる種類のアプリを作成できます。&ndash;

アプリ開発に慣れていない場合でも、単一のデータ ソースを基にアプリを自動作成することで、シンプルなアプリの作成方法を確認でき、その後ニーズに合わせてカスタマイズできます。 このビデオではその方法を 5 分で紹介します:

[!VIDEO nb:cid:UUID:34ccfd46-7826-49ce-90d8-cf6a144b6968]


たとえばカスタムの SharePoint リストから**[アプリを自動作成した](app-from-sharepoint.md)**後に、アプリでの**[すべての項目](customize-layout-sharepoint.md)**、**[各項目の詳細](customize-forms-sharepoint.md)**、**[項目の作成または編集のオプション](customize-forms-sharepoint.md)**の表示方法を変更できます。 また、**[サンプル アプリ](open-and-run-a-sample-app.md)**や**[テンプレート](get-started-test-drive.md)**を開いて PowerApps で実現可能なことを確認したり、より複雑なアプリを作成する方法を学んだりすることもできます。

ある程度の経験や創造性があれば、**[独自のアプリをゼロから作成](get-started-create-from-blank.md)**できます。 **[数式を作成](working-with-formulas.md)**することで、**[データ ソース](connections-list.md)**への接続、**[UI 要素の追加](reference-properties.md)** (コントロールと呼ばれます)、アプリの動作の指定を行うことができます。 小さなアプリから初めて自分のペースでスキルを身に付けることで、組織におけるデータの管理方法を刷新するアプリを構築して共有できるようになります。 最初の一歩を踏み出す用意はできましたか?

## <a name="generate-an-app-automatically"></a>アプリを自動的に生成する
アプリを自動的に生成するには、次のいずれかのデータ ソースを指定します。

* **[Common Data Service](data-platform-intro.md)**
* SQL Server データベース
* Salesforce
* Dynamics 365
* Excel ワークブック (クラウドストレージ アカウントの場合)

具体的な手順については、**[SharePoint のデータを管理するアプリの作成](app-from-sharepoint.md)**に関するページを参照してください。 SharePoint を想定して執筆されていますが、他の種類のデータ ソースでも基本的な手順は同じです。

## <a name="customize-an-app"></a>アプリをカスタマイズする
生成されたアプリが、そのままでは実際の用途に合わない場合、アプリを**[カスタマイズ](customize-layout-sharepoint.md)**することができます。 たとえば、異なるコントロールで異なるデータや同じデータを表示させたい、といったケースが考えられます。

より良いアプリにするためのアイデアについては、**[サンプル アプリ](open-and-run-a-sample-app.md)**を開いてみてください。ある程度の創造性と少しの経験で生み出すことができる何かを感じ取ることができるでしょう。

![サンプル アプリ](./media/getting-started/portal-home.png)

**[アプリはテンプレートから作成](get-started-test-drive.md)**することもできます。 それぞれのテンプレートには、Dropbox などのクラウド アカウント内の架空データが使われています。 特定の画面やコントロールを観察してその構成方法についての理解を深め、実際にカスタマイズしてみることによって独自のアプリに適用できる手法を発見してください。

## <a name="create-an-app-from-scratch"></a>アプリを最初から作成する
アプリを自動的に生成する作業を 1、2 回経験し、カスタマイズのノウハウがある程度得られたら、**[アプリを最初から作成](get-started-create-from-blank.md)**してみましょう。 何もない状態から作業することで、アプリの設計やフロー、制御の幅が広がり、組み込むことができる**[データ ソース](connections-list.md)**の種類も増えます。

いくつかの必要な概念について詳しくは、以下のトピックをご覧ください。

* 数式 (**[チュートリアル](working-with-formulas.md)**または**[リファレンス](formula-reference.md)**)
* ギャラリー (**[チュートリアル](add-gallery.md)**または**[リファレンス](reference-properties.md)**)
* フォーム (**[チュートリアル](add-form.md)**または**[リファレンス](working-with-forms.md)**)
* **[テーブルとレコード](working-with-tables.md)**
* **[コントロールとそのプロパティ](reference-properties.md)**

## <a name="share-and-run-an-app"></a>アプリの共有と実行
完成したアプリは、組織内の同僚と**[共有](share-app.md)**することができます。自分が作成したアプリや他人によって共有されたアプリを**[ブラウザー](run-app-browser.md)**または**[携帯電話](run-app-client.md)**で実行することができます。

## <a name="more-information"></a>詳細
このトピックでは PowerApps でできることの概要を大まかに示しましたが、可能性は無限大です。 このページの左側にある各トピックで、詳細な手順と参考情報を確認できます。 本トピックでは解決できない詳細な質問がある場合には、以下のようにしてください。

* **[PowerApps のコミュニティに参加](https://aka.ms/powerapps-community)**して、他の PowerApps ユーザーに質問する、または意見交換する。
* **[サポートに問い合わせる](https://aka.ms/pasupport)**。

