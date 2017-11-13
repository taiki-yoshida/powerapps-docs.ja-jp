---
title: "ルールの作成 | Microsoft Docs"
description: "ルールを作成してアプリ ロジックを構築するための詳しい手順"
services: 
suite: PowerApps
documentationcenter: na
author: karthik-1
manager: anneta
editor: 
tags: 
ms.service: powerapps
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 09/14/2017
ms.author: karthikb
ms.openlocfilehash: c6b7141c20591c1fdbb5278b1fe4d75bfb6a4ebb
ms.sourcegitcommit: 43be6a4e08849d522aabb6f767a81c092419babc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2017
---
# <a name="create-a-rule-in-powerapps"></a>PowerApps でのルールの作成
指定した条件に基づいてアプリを自動的に変更するためのルールを作成します。 たとえば、状態に基づいてリスト項目を赤、黄、または緑で表示したり、特定のユーザー (管理者など) に対してのみ承認ボタンを表示したりします。

ルールは、さまざまなコントロールに追加できます。 このトピックでは、**スライダー** コントロールの値が 70 を超えている場合に、**ラベル**のテキストの色を変更するルールを追加します。

## <a name="add-a-rule"></a>ルールの追加
1. コントロールを選択します (またはコントロールを追加し、選択されたままにします)。
   
    このトピックでは、[ラベルとスライダーを追加](add-configure-controls.md)して、ラベルの **Text** プロパティを **Slider1.Value** に設定し、スライダーを選択します。
2. 右側のパネルで、**[ルール]** をクリックまたはタップして、**[新しいルール]** をクリックまたはタップします。
   
    ![新しいルールの作成](./media/working-with-rules/new-rule.png)
   
    1 つまたは複数のルールが既に定義されているコントロールを選択すると、クリックまたはタップで、それらのうちのどれでも編集することができます。  

## <a name="add-a-condition"></a>条件の追加
条件とは、true または false を評価する式です (値が 70 を超えているかどうかなど)。 テンプレートに基づいて、または最初から式を記述して、UI (Intellisense) のガイダンスに基づいて式をカスタマイズできます。

1. **[条件の追加]** をクリックまたはタップして、テンプレートをクリックするか、または **[ユーザー設定条件]** をクリックします。
   
    このトピックでは、**[次の値より大きい]** をクリックまたはタップします。
   
    ![条件の追加](./media/working-with-rules/rule-conditions.png)
2. どのような場合にルールを適用するかを定義する式を完成させます。
   
    このトピックでは、次の式を使用します。 <br>**Value(Slider1.Value) > 70**
   
    **注**: この記事の執筆時点では、比較に使用されるコントロールのプロパティを指定する必要があります。 将来のリリースでは、PowerApps はコントロールの共通プロパティ (**Text** または **Value** など) を推測するようになる可能性があります。

## <a name="add-an-action"></a>アクションの追加
アクションは、ルールが適用されたときの動作を定義します。 PowerApps では、コントロールに加えた変更に基づいて、自動的にアクションを作成できます。

1. **[アクションの定義]** をクリックまたはタップします。
   
    ![アクションの定義](./media/working-with-rules/rule-define-actions.png)
2. 確認ダイアログ ボックスで **[始めましょう]** をクリックまたはタップして、PowerApps で次の変更を 1 つまたは複数のアクションとしてキャプチャできるようにします。
3. 条件が true のときに希望通りに動作するように、1 つまたは複数のコントロールを構成します。
   
    このトピックでは、ラベルの色を変更します。
   
    ![プロパティのキャプチャ](./media/working-with-rules/rule-capture-properties.png)
4. (省略可能) **[アクションの表示]** をクリックまたはタップして、変更を確認します。
   
    ![アクションの確認](./media/working-with-rules/rule-review-actions.png)
5. アクションの追加が完了したら、**[完了]** をクリックまたはタップします。
6. ルールの条件とアクションを確認し、**[完了]** をクリックまたはタップして保存します。
   
    ![ルールの確認](./media/working-with-rules/rule-review.png)

## <a name="test-the-rule"></a>ルールのテスト
1. F5 キーを押して (または右上隅の再生ボタンをクリックして) アプリをプレビューします。
   
    ![プレビューを開く](./media/working-with-rules/open-preview.png)
2. true に指定した条件を作成し、アクションが希望通りに動作することを確認します。
   
    このトピックでは、スライダーを 70 よりも大きい値に設定して、ラベルのテキストの色が変わることを確認します。

## <a name="known-limitations"></a>既知の制限
この記事の執筆時点では、次のものがあります。

* ルールの名前は変更できません。
* 条件の一部として、フォームまたはギャラリーの **ThisItem** プロパティを指定することはできません。

