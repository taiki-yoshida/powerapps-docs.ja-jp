---
title: Download、Launch、および Param 関数 | Microsoft Docs
description: 構文と例を含む PowerApps の Download、Launch、および Param 関数の参照情報
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
ms.openlocfilehash: 4ed646431263e96a079483bc514c8154b6d9b653
ms.sourcegitcommit: 59785e9e82da8f5bd459dcb5da3d5c18064b0899
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/22/2018
---
# <a name="download-launch-and-param-functions-in-powerapps"></a>PowerApps の Download、Launch、および Param 関数
パラメーターを使用して、Web ページまたはアプリをダウンロードまたは起動します。  

## <a name="description"></a>説明
**Download** 関数は、Web からローカル デバイスにファイルをダウンロードします。  ユーザーは、ファイルを保存する場所の入力を求められます。  **Download** は、ファイルが格納されているローカルの場所を文字列として返します。  

**Launch** 関数は、Web ページまたはアプリを起動します。  この関数では、必要に応じて、アプリにパラメーターを渡すことができます。  

**Param** 関数は、アプリに渡されたパラメーターをアプリの起動時に取得します。  名前付きパラメーターが渡されていなかった場合、**Param** は "*空白*" を返します。

## <a name="syntax"></a>構文
**Download**( *Address* )

* *Address* - 必須。  ダウンロードする Web リソースのアドレス。

**Launch**( *Address* [, *ParameterName1*, *ParameterValue1*, ... ] )

* *Address* - 必須。  起動する Web ページのアドレスまたはアプリの ID。
* *ParameterName(s)* - 省略可能。  パラメーター名。
* *ParameterValue(s)* - 省略可能。  アプリまたは Web ページに渡す、対応するパラメーター値。

**Param**( *ParameterName* )

* *ParameterName* - 必須。  アプリに渡されるパラメーターの名前。

