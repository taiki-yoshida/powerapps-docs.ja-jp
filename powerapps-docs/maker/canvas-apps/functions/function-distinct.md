---
title: Distinct 関数 | Microsoft Docs
description: 構文と例を含む PowerApps の Distinct 関数の参照情報
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
ms.openlocfilehash: 820ae85b99e0a8bab8ff2cf8308540336dee60af
ms.sourcegitcommit: 59785e9e82da8f5bd459dcb5da3d5c18064b0899
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/22/2018
---
# <a name="distinct-function-in-powerapps"></a>PowerApps の Distinct 関数
重複を削除して、[テーブル](../working-with-tables.md)の[レコード](../working-with-tables.md#records)を要約します。

## <a name="description"></a>説明
**Distinct** 関数は、テーブルの各レコードで数式を評価します。 **Distinct** は、重複する値が削除された結果を含む 1 列のテーブルを返します。  

[!INCLUDE [record-scope](../../../includes/record-scope.md)]

## <a name="syntax"></a>構文
**Distinct**( *Table*, *Formula* )

* *Table* - 必須。  全体を評価するテーブル。
* *Formula* - 必須。  各レコードについて評価する数式。

## <a name="example"></a>例
**Department** 列が含まれている **Employees** テーブルがある場合、この関数はこの列内の各部署名を一覧表示します。この列で各名前が何回か出現していても、一覧では重複しないように表示されます。

**Distinct(Employees, Department)**

