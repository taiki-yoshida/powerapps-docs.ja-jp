---
title: "PowerApps の新機能 | Microsoft Docs"
description: "PowerApps の更新内容 (リリースの日付順)"
services: 
suite: powerapps
documentationcenter: na
author: skjerland
manager: anneta
editor: 
tags: 
ms.service: powerapps
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 02/13/2018
ms.author: sharik
ms.openlocfilehash: b8d06bb8ffbe1446f4c918e6cf1c6657c1890e65
ms.sourcegitcommit: e827813cd898ca9a1046b5952ea5e32ce2989a65
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/14/2018
---
# <a name="whats-new-in-powerapps"></a>PowerApps の新機能
既知の制限については、「[Common issues and resolutions (お問い合わせの多い問題と解決方法)](common-issues-and-resolutions.md)」を参照してください。

> [!NOTE]
> リリースは、数日間にわたってロールアウトします。 新機能や更新された機能は、すぐには表示されない場合があります。

## <a name="feb-12"></a>2 月 12 日
* 埋め込まれた[ビデオ](controls/control-audio-video.md)および[オーディオ](controls/control-audio-video.md)の再生用ボリューム コントロールがインラインになりました。 再生をミュートにするには、ユーザーはボタンをクリックまたはタップする代わりに、ボリューム コントロールを使用してボリュームを下げる必要があります。

## <a name="feb-7"></a>2 月 7 日
1. [カメラ](controls/control-camera.md)および[バーコード スキャナー](controls/control-barcodescanner.md)のコントロールから、ズーム、明るさおよびコントラストのプロパティを削除しました。
2. [テキスト入力](controls/control-text-input.md)コントロールのクリア ボタンがユーザー入力に割り当てられた領域を制限する問題を解決しました。 この修正によって、テキスト入力コントロールの[クリア](controls/control-text-input.md#additional-properties) プロパティは、Microsoft Edge (最新バージョン) および Internet Explorer 11 Web ブラウザーでのみサポートされます。
3. アクセシビリティの機能強化が[マルチメディア](add-images-pictures-audio-video.md) コントロールに追加されました。

## <a name="jan-31"></a>1 月 31 日
1. [ビデオ](controls/control-audio-video.md)コントロールにクローズド キャプションが追加されました。
2. [PDF ビューアー](controls/control-pdf-viewer.md)コントロールのエラー処理が向上しました。

## <a name="jan-18"></a>1 月 18 日
1. PowerApps for iOS と PowerApps for Android での Microsoft Authenticator との統合がサポートされました。
2. フォームの [SharePoint lookup コントロール](sharepoint-lookup-fields.md)が[コンボ ボックス](controls/control-combo-box.md)に置き換えられ、PowerApps Studio の単一選択 lookup フィールドに、新しい[データ カード](working-with-cards.md) テンプレートが既定で選択されます。
3. 拡張された読み取りモードを使用すると、[コンボ ボックス](controls/control-combo-box.md)内の候補リストにすべての項目が表示されます。
4. [委任不可のクエリ](delegation-overview.md#non-delegable-limits)におけるローカル レコードの保存上限サイズを、最大 2000 レコードまでに制御できます。 (実験的な機能)

## <a name="jan-5"></a>1 月 5 日
* Power BI レポートからコンテキスト データを取得する [PowerApps カスタム ビジュアル (プレビュー リリース)](https://powerapps.microsoft.com/blog/powerbi-powerapps-visual/) を統合したことで、Power BI レポートやダッシュボードのデータに基づいて行動できます。

## <a name="dec-8"></a>12 月 8 日
1. ルール用の[条件テンプレート](working-with-rules.md)により、コントロール共通のプロパティを推定します (**テキスト**または**値**など)。
2. ルールのアクションを定義する際の、[**アクションの定義**の確認ダイアログ ボックス](working-with-rules.md)が表示されないようにしました。

## <a name="nov-13"></a>11 月 13 日
1. SharePoint リストで、同じフィールドに複数の値を選択できます。
2. SharePoint リストで、[添付ファイルの表示とダウンロード](controls/control-attachments.md)を行うことができます。
3. PowerApps を使用して [SharePoint リスト フォームをカスタマイズ](customize-list-form.md)できます。

## <a name="nov-10"></a>11 月 10 日
* アプリの[ルール名を変更](working-with-rules.md)し、選択したコントロールがルールの条件にある場合に、ルールを表示します。

## <a name="oct-30"></a>10 月 30 日
1. アプリで、選択したコントロールのルールだけでなく、[すべてのルールを表示](working-with-rules.md)します。
2. アプリ作成者から最も要望が多かったアイコンを追加します。
3. Android および iOS デバイスでのアプリのパフォーマンスが向上しました。

## <a name="sept-20"></a>9 月 20 日
1. 最初に[アプリを保存](save-publish-app.md)したあとは、追加の変更が既定で 2 分おきに自動的に保存されます。
2. 式の記述をせずに、簡単に条件付き書式の[ルールを作成](working-with-rules.md)できます。PowerApps キャンバス上で条件を設定し、結果を設計するだけです。
3. コントロールが追加されたときに別ウィンドウに表示される全画面のデータ ペインで、フォーム、ギャラリー、およびデータ テーブルをより簡単に構成できます。
4. 空のアプリ、テンプレート、データ ソース、または SharePoint のいずれから開始する場合でも、アプリの作成に役立つ状況に合わせたクイック ヒントが表示されます。

## <a name="sept-6"></a>9 月 6 日
1. 作成したアプリについては、Power BI での埋め込みダッシュ ボードで[使用状況を追跡](app-analytics.md)します。
2. 区切り記号を使用してテキスト文字列を分割するには、**[Split](functions/function-split.md)** 関数を使用します。
