---
title: "Attachments コントロール: リファレンス | Microsoft Docs"
description: "各種プロパティとサンプルを含む Attachments コントロールに関する情報"
services: 
suite: powerapps
documentationcenter: na
author: fikaradz
manager: anneta
editor: 
tags: 
ms.service: powerapps
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 09/29/2017
ms.author: fikaradz
ms.openlocfilehash: 2fd5db380eead5403d4cc7d927da5a24aa24abc9
ms.sourcegitcommit: 33099e6197c0139679cd08c42e9e2a5717904c92
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/12/2018
---
# <a name="attachments-control-in-powerapps"></a>PowerApps の Attachments コントロール
ユーザーが自分のデバイスにファイルをダウンロードできるコントロールです。  アップロード機能はまもなく公開されます。

## <a name="description"></a>説明
**Attachments** コントロールでは、データ ソースに格納されているファイルを開くことができます。

## <a name="key-properties"></a>主要なプロパティ
**[Items](properties-core.md)** – ダウンロードできるファイルを記述するソースです。

**MaxAttachments** - コントロールが受け入れるファイルの最大数です。

**OnAttach** – ユーザーが新しい添付ファイルを追加したときのアプリの応答です。

**OnRemove** – ユーザーが既存の添付ファイルを削除したときのアプリの応答です。

**[OnSelect](properties-core.md)** – ユーザーが添付ファイルをクリックしたときのアプリの応答です。

## <a name="additional-properties"></a>その他のプロパティ
**AddAttachmentText** – 新しい添付ファイルを追加するために使用するボタンのラベル テキストです。

**[BorderColor](properties-color-border.md)** – コントロールの境界線の色です。

**[BorderStyle](properties-color-border.md)** – コントロールの境界線を **Solid** (実線)、**Dashed** (破線)、**Dotted** (点線)、**None** (なし) のいずれに指定します。

**[BorderThickness](properties-color-border.md)** – コントロールの境界線の太さです。

**[DisplayMode](properties-core.md)** – コントロールで、ユーザー入力を許可するか (**Edit**)、データの表示のみを許可するか (**View**)、許可しないか (**Disabled**) を設定します。

**[Height](properties-size-location.md)** – コントロールの上端と下端の距離です。

**NoAttachmentsText** – 表示する添付ファイルが存在しないときにユーザーに表示する指示テキストです。

**[Visible](properties-core.md)** – コントロールを表示するか非表示にするかです。

**[Width](properties-size-location.md)** – コントロールの左端と右端の間の距離です。

**[X](properties-size-location.md)** – コントロールの左端とその親コンテナー (親コンテナーがない場合は画面) の左端間の距離です。

**[Y](properties-size-location.md)** – コントロールの上端とその親コンテナー (親コンテナーがない場合は画面) の上端間の距離です。


## <a name="example"></a>例
1. データ ソースとして SharePoint リストを使用してデータからアプリを作成します。  または、アプリにフォームを追加し、そのデータ ソースとして SharePoint リストを設定します。

2. 左側にあるツリー ビュー内の **Form** コントロールを選択します。

3. 右側の [オプション] パネルの [プロパティ] タブで **[データ]** をクリックします。

4. **[フィールド]** の下で、**[添付ファイル]** フィールドを有効にします。

    SharePoint リストに関連付けられている添付ファイル フィールドが、フォームに表示されます。

[コントロールの追加および構成](../add-configure-controls.md)についてはこちらをご覧ください。
