---
title: SaveData および LoadData 関数 | Microsoft Docs
description: 構文を含む PowerApps の SaveData および LoadData 関数の参照情報
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
ms.openlocfilehash: aa62882841ee4d585720a2241dff8b9f35c88059
ms.sourcegitcommit: 59785e9e82da8f5bd459dcb5da3d5c18064b0899
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/22/2018
---
# <a name="savedata-and-loaddata-functions-in-powerapps"></a>PowerApps の SaveData および LoadData 関数
[コレクション](../working-with-data-sources.md#collections)を保存および再読み込みします。

## <a name="description"></a>説明
**SaveData** 関数は、後で名前から使用できるようにコレクションを格納します。  

**LoadData** 関数は、既に **SaveData** で保存されている名前でコレクションを再読み込みします。 別のソースからコレクションを読み込む場合、この関数は使用できません。  

**LoadData** はコレクションを作成しません。この関数は、既存のコレクションの格納しか行いません。 最初に **[Collect](function-clear-collect-clearcollect.md)** を使用して、適切な[列](../working-with-tables.md#columns)でコレクションを作成する必要があります。

ストレージは暗号化され、他のユーザーとアプリからは分離された、ローカル デバイス上のプライベートな場所にあります。  

## <a name="syntax"></a>構文
**SaveData**( *Collection*, *Name* )<br>**LoadData**( *Collection*, *Name* [, *IgnoreNonexistentFile* ])

* *Collection* - 必須。  格納または読み込みの対象となるコレクション。
* *Name* - 必須。  ストレージの名前。 同じデータ セットを保存し、読み込むには、同じ名前を使用する必要があります。 名前空間は、他のアプリまたはユーザーとは共有されません。
* *IgnoreNonexistentFile* - 省略可能。 一致するファイルが見つからないときに **LoadData** 関数でエラーを表示するか無視するかを示すブール値 (**true**/**false**)。 **false** を指定した場合、エラーが表示されます。 **true** を指定した場合、エラーは無視されます。これは、オフラインのシナリオで役立ちます。 **SaveData** は、デバイスがオフライン (つまり、**Connection.Connected** の状態が **false**) の場合に、ファイルを作成します。

## <a name="examples"></a>例
| 数式 | 説明 | 結果 |
| --- | --- | --- |
| **If(Connection.Connected, ClearCollect(LocalTweets, Twitter.SearchTweet("PowerApps", {maxResults: 100})),LoadData(LocalTweets, "Tweets", true))** |デバイスが接続されている場合、Twitter サービスから LocalTweets コレクションを読み込みます。それ以外の場合は、ローカル ファイル キャッシュからコレクションを読み込みます。 |デバイスがオンラインであるかオフラインであるかによって、コンテンツがレンダリングされます。 |
| **SaveData(LocalTweets, "Tweets")** |LocalTweets コレクションをデバイスにローカル ファイル キャッシュとして保存します。 |**LoadData** がコレクションに読み込むことができるように、データはローカルに保存されます。 |

