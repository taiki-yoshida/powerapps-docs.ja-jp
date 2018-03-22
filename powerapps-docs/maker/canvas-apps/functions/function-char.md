---
title: Char 関数 | Microsoft Docs
description: 構文と例を含む PowerApps の Char 関数の参照情報
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
ms.date: 11/07/2015
ms.author: gregli
ms.openlocfilehash: 7ce510840845b1a1df2d590c4f3ffdddfc5bfb9c
ms.sourcegitcommit: 59785e9e82da8f5bd459dcb5da3d5c18064b0899
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/22/2018
---
# <a name="char-function-in-powerapps"></a>PowerApps の Char 関数
文字コードを文字列に変換します。

## <a name="description"></a>説明
**Char** 関数は、プラットフォームの適切な ASCII 文字を含む文字列を返します。

## <a name="syntax"></a>構文
**Char**( *CharacterCode* )

* *CharacterCode* - 必須。 変換する ASCII 文字コード。

## <a name="examples"></a>例
| 数式 | 説明 | 結果 |
| --- | --- | --- |
| **Char( 65 )** |ASCII コード 65 に対応する文字を返します。 |A |
| **Char( 105 )** |ASCII コード 105 に対応する文字を返します。 |i |
| **Char( 35 )** |ASCII コード 35 に対応する文字を返します。 |# |

