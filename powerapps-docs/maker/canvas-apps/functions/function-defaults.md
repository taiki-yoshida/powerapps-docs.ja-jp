---
title: Defaults 関数 | Microsoft Docs
description: 構文と例を含む PowerApps の Defaults 関数の参照情報
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
ms.date: 11/01/2015
ms.author: gregli
ms.openlocfilehash: eb1c6b802eff4aa5bd02a2ec52626b8788c42b73
ms.sourcegitcommit: 59785e9e82da8f5bd459dcb5da3d5c18064b0899
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/22/2018
---
# <a name="defaults-function-in-powerapps"></a>PowerApps の Defaults 関数
[データ ソース](../working-with-data-sources.md)の既定値を返します。  

## <a name="description"></a>説明
**Defaults** 関数を使用して、データ入力フォームに事前に値を設定し、入力の手間を軽減します。

この関数は、データ ソースの既定値が含まれている[レコード](../working-with-tables.md#records)を返します。  データ ソース内の[列](../working-with-tables.md#columns)に既定値がない場合、そのプロパティは存在しません。

データ ソースが提供する既定の情報の量は、データ ソースによって異なります。まったく情報を提供しないデータ ソースもあります。  既定値をサポートしていない[コレクション](../working-with-data-sources.md#collections)やその他のデータ ソースが操作対象となった場合、**Defaults** 関数は[空](function-isblank-isempty.md)のレコードを返します。

[レコードを作成する](../working-with-data-sources.md)ために、**Defaults** 関数と **[Patch](function-patch.md)** 関数を組み合わせることができます。

## <a name="syntax"></a>構文
**Defaults**( *DataSource* )

* *DataSource* – 必須。 既定値の提供元となるデータ ソース。

## <a name="examples"></a>例
| 数式 | 説明 | 結果 |
| --- | --- | --- |
| **Defaults(&nbsp;Scores&nbsp;)** |**Scores** データ ソースの既定値を返します。 |**{ Score: 0 }** |

