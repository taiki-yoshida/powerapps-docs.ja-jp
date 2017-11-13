---
title: "EncodeUrl および PlainText 関数 | Microsoft Docs"
description: "構文と例を含む PowerApps の EncodeUrl および PlainText 関数の参照情報"
services: 
suite: powerapps
documentationcenter: na
author: gregli-msft
manager: anneta
editor: 
tags: 
ms.service: powerapps
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 11/07/2015
ms.author: gregli
ms.openlocfilehash: a511d731c8dd94c57ec9846d853fec1bef10ab0a
ms.sourcegitcommit: 43be6a4e08849d522aabb6f767a81c092419babc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2017
---
# <a name="encodeurl-and-plaintext-functions-in-powerapps"></a>PowerApps の EncodeUrl および PlainText 関数
文字列をエンコードおよびデコードします。

## <a name="description"></a>説明
**EncodeUrl** 関数は、英数字以外の文字を % と 16 進数に置き換えることで URL 文字列をエンコードします。  

**PlainText** 関数は、次のようなタグを適切な記号に変換して、HTML および XML タグを削除します。

* **&amp;nbsp;**
* **&amp;quot;**

これらの関数からの戻り値は、エンコードまたはデコードされた文字列です。   

## <a name="syntax"></a>構文
**EncodeUrl**( *String* )

* *String* - 必須。  エンコードする URL。

**PlainText**( *String* )

* *String* - 必須。 HTML および XML タグが削除される文字列。

## <a name="examples"></a>例
テキスト ギャラリーに RSS フィードを表示し、そのギャラリーのラベルの **[Text](../controls/properties-core.md)** プロパティを **ThisItem.description** に設定した場合、ラベルには次の例のように未加工の HTML または XML コードが表示される可能性があります。

    <p>We have done an unusually&nbsp;&quot;deep&quot; globalization and localization.<p>

ラベルの **[Text](../controls/properties-core.md)** プロパティを **PlainText(ThisItem.description)** に設定すると、次の例のようなテキストが表示されます。

    We have done an unusually "deep" globalization and localization.
