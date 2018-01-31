---
title: "カードのカスタマイズ | Microsoft Docs"
description: "カードに対する基本的なカスタマイズと高度なカスタマイズを実行する"
services: 
suite: powerapps
documentationcenter: 
author: skjerland
manager: anneta
editor: 
tags: 
ms.service: powerapps
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/30/2016
ms.author: sharik
ms.openlocfilehash: 9fdde89b254e491f2dc333261649df7fd156f2c2
ms.sourcegitcommit: 6afca7cb4234d3a60111c5950e7855106ff97e56
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2018
---
# <a name="customize-a-card-in-microsoft-powerapps"></a>Microsoft PowerApps におけるカードのカスタマイズ
基本的なカスタマイズ (カードのロック解除を伴わないカスタマイズ) は、コントロールの変更などによって行います。 高度なカスタマイズは、カードのロックを解除し、既定では利用できないコントロールをカードに追加するなどして行います。

概要については、「[Understand data cards (データ カードについて)](working-with-cards.md)」をご覧ください。

## <a name="prerequisites"></a>前提条件

* [コントロールを追加して構成](add-configure-controls.md)する方法について学ぶ。
* このトピックでは、一般的な概念のみを確認できます。 (順を追って) 正確に実行するには、次のトピックの手順に従ってください。

  1. [SharePoint からアプリを作成する](app-from-sharepoint.md)。
  2. [レイアウトをカスタマイズする](customize-layout-sharepoint.md)。
  3. [フォームをカスタマイズする](customize-forms-sharepoint.md)。

## <a name="customize-a-locked-card"></a>ロックされたカードのカスタマイズ
この手順では、カードのロックを解除せずに、**[トグル](controls/control-toggle.md)** コントロールを**[ラジオ](controls/control-radio.md)** コントロールで置き換えます。

1. **EditScreen1** で、**Paid** カードをクリックまたはタップして選択します。

    ![](./media/customize-card/select-paid-card.png)

2. 右側のウィンドウで、**Paid** カードのカード セレクターをクリックまたはタップし、**[オプションの編集]** をクリックまたはタップします。

    ![](./media/customize-card/select-toggle-paid.png)

    画面に変更内容が反映されます。

    ![](./media/customize-card/display-radio.png)
   
    SharePoint の列の種類ごとにサポートされるカードの種類については、「[Known issues (既知の問題)](connections/connection-sharepoint-online.md#known-issues)」を参照してください。

## <a name="unlock-and-customize-a-card"></a>カードのロック解除とカスタマイズ
この手順では、カードのロックを解除し、**[テキスト入力](controls/control-text-input.md)**コントロールを**[スライダー](controls/control-slider.md)** コントロールで置き換えます。

1. **EditScreen1** で、**Quantity** カードをクリックまたはタップします。

2. 右側のウィンドウで、そのカードに対応する省略記号アイコンをクリックまたはタップし、**[詳細オプション]** をクリックまたはタップします。

    ![詳細オプションを開く](./media/customize-card/advanced-options.png)
3. 右側のウィンドウの一番上にあるロック アイコンをクリックまたはタップしてカードのロックを解除します。

    ![カードのロックを解除](./media/customize-card/unlock-card.png)
4. カードで、**テキスト入力**コントロールを削除し、**スライダー** コントロールを追加して、新しいコントロールに「**QtySlider**」と名前を付けます。

5. 右側のウィンドウで **Quantity** カードの **[更新]** プロパティに次の式を設定します。<br>
   **QtySlider.Value**

   > [!NOTE]
> **[更新]** プロパティが表示されない場合は、**[データ]** セクションの一番下にある **[More options (その他のオプション)]** をクリックまたはタップします。


6. スライダーをクリックまたはタップして選択し、右側のウィンドウの一番上にあるコントロールの一覧を開きます。

7. **[ErrorMessage4]** をクリックまたはタップし、その **[高さ]** プロパティに次の式を設定します。<br>
   **QtySlider.Y + QtySlider.Height**
