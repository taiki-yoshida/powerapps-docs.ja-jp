---
title: "Enable および Disable 関数 | Microsoft Docs"
description: "構文と例を含む PowerApps の Enable および Disable 関数の参照情報"
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
ms.openlocfilehash: b4051bdb312707cfafe63a97b5e77a2860feb60c
ms.sourcegitcommit: 43be6a4e08849d522aabb6f767a81c092419babc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2017
---
# <a name="enable-and-disable-functions-in-powerapps"></a>PowerApps の Enable および Disable 関数
[シグナル](signals.md) を有効または無効に切り替えます。

## <a name="overview"></a>概要
いくつかのシグナルは頻繁に変化する場合があるため、アプリはその度に再計算を行う必要があります。  長期間にわたる頻繁な変更によって、デバイスのバッテリが消耗することがあります。 これらの関数を使用すると、手動でシグナルを有効または無効にすることができます。

シグナルは使用されていない場合、自動的に無効になります。

## <a name="description"></a>説明
**Enable** 関数と **Disable** 関数はそれぞれ、シグナルを有効および無効に切り替えます。

これらの関数は、現在、**[Location](signals.md)** シグナルのみに有効です。

これらの関数には、戻り値がありません。 これらの関数は、[動作の数式](../working-with-formulas-in-depth.md#behavior-formulas)内でのみ使用できます。

## <a name="syntax"></a>構文
**Enable**( *Signal* )<br>**Disable**( *Signal* )

* *Signal* - 必須。  有効または無効にするシグナル。

