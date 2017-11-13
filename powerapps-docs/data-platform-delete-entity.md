---
title: "カスタム エンティティの削除とデータの消去 | Microsoft Docs"
description: "カスタム エンティティを削除し、すべてのデータを消去します。"
services: powerapps
documentationcenter: na
author: kfend
manager: kfend
editor: 
tags: 
ms.service: powerapps
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 12/06/2016
ms.author: kfend
ms.openlocfilehash: 2c0dbc172ee7354bc94670f9bb6993d33fca8f2c
ms.sourcegitcommit: 43be6a4e08849d522aabb6f767a81c092419babc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2017
---
# <a name="delete-a-custom-entity"></a>カスタム エンティティの削除
カスタム エンティティは削除できますが、標準エンティティは削除できません。

1. [powerapps.com](https://web.powerapps.com) で、**[Common Data Service]** セクションを展開し、左側のナビゲーション ウィンドウで **[エンティティ]** をクリックまたはタップします。 エンティティ一覧は、その上に表示される検索バーに文字を入力してフィルタリングできます。
2. エンティティの一覧で、削除するエンティティをクリックまたはタップし、右上隅のごみ箱ボタンをクリックまたはタップします。
3. 表示されたダイアログ ボックスで、**[削除]** をクリックまたはタップするとエンティティが削除されます。

## <a name="notes"></a>メモ
* エンティティを削除すると、エンティティの定義と、エンティティに含まれるすべてのデータの両方が削除されます。
* アプリで使用されているエンティティを削除すると、アプリが正常に動かなくなる可能性があります。
* エンティティ A にエンティティ B の[ルックアップ フィールド](data-platform-entity-lookup.md)が存在する場合、エンティティ A を削除するためには、先にエンティティ B を削除しなければならないことがあります。

