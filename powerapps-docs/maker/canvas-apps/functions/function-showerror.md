---
title: ShowError 関数 | Microsoft Docs
description: 構文と例を含む PowerApps の ShowError 関数の参照情報
services: ''
suite: powerapps
documentationcenter: na
author: gregli-msft
manager: anneta
editor: ''
tags: ''
ms.service: powerapps
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 03/21/2018
ms.author: gregli
ms.openlocfilehash: 7c1d5a8c7b35d316a2720d564977170029e28359
ms.sourcegitcommit: a9d33322228c398d29964429602dc3fe19fa67d2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/28/2018
---
# <a name="showerror-function-in-powerapps"></a>PowerApps の ShowError 関数
ユーザーにエラーが表示されます。

## <a name="description"></a>説明
**ShowError** 関数では、ユーザーにエラーが表示されます。  アプリの作成中と、エンド ユーザーがアプリを使用しているときの両方でメッセージが表示されます。

**ShowError** は、[動作の数式](../working-with-formulas-in-depth.md)内でのみ使用できます。

**ShowError** は、常に *true* を返します。

**ShowError** は [**IfError**](function-iferror.md) 関数と組み合わせて、エラーを検出し、カスタム エラー メッセージを使って報告することができます。

## <a name="syntax"></a>構文
**ShowError**( *Message* )

* *Message* - 必須。  ユーザーに表示するメッセージです。 

## <a name="examples"></a>例

### <a name="step-by-step"></a>ステップ バイ ステップ

1. 画面に**ボタン** コントロールを追加します。

2. **Button** の **OnSelect** プロパティを次のように設定します。

    **ShowError( "Hello, World" )**

3. ボタンをクリックするか、押します。  

    ボタンがクリックされるたびに、**Hello, World** のメッセージがユーザーに表示されます。

    ![作成環境で、ボタンが表示され、OnSelect により ShowError が呼び出されて、その結果ユーザーに対して赤いバナー メッセージで「Hello, World」のメッセージが表示されているところ](media/function-showerror/hello-world.png)
