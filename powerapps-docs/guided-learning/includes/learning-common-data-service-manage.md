このトピックでは、Common Data Service でのデータ管理を取り上げます。 データのインポートおよびエクスポートについては他のトピックでも取り上げてきましたが、ここでは Excel でのデータ操作についてより多くの時間をとります。

## <a name="import-data-from-excel-or-csv"></a>Excel または CSV からデータをインポートする
この例では、Excel から 1 つ前のトピックで作成した Product review (製品のレビュー) エンティティにデータをインポートします。 データは、CSV ファイルからもインポートできます。CSV はデータを移動するための共通の形式です。 ここで、エンティティの外観を確認しましょう。強調表示されている領域がこのトピックで注目する領域です。

![Product review (製品のレビュー) エンティティ](./media/learning-common-data-service-manage/product-review-entity.png)

エンティティ内の **[Import data]** (データのインポート) をクリックして、インポート元のファイルに移動します。 **[Show mapping]** (マッピングの表示) をクリックして、Excel ファイル内の列がエンティティの正しいフィールドに関連付けられていることを確認します。 マッピングが完了したら、**[Save changes]** (変更の保存) をクリックします。 メインのインポート画面に戻って、**[Import]** (インポート) をクリックします。

![Excel からデータをインポートする](./media/learning-common-data-service-manage/import-data.png)

## <a name="export-data-to-excel"></a>Excel にデータをエクスポートする
Common Data Service の外でデータにアクセスする必要がある場合は、データをエクスポートします。 エンティティ内の **[Export Data]** (データのエクスポート) をクリックして、zip ファイルが生成されるまで待ちます。 zip ファイルを開いて、エクスポートされたデータを確認します。 
![Excel にデータをエクスポートする](./media/learning-common-data-service-manage/export-data.png)

## <a name="export-a-template-to-excel"></a>Excel にテンプレートをエクスポートする
データをダウンロードするほかに、テンプレートをダウンロードすることができます。 テンプレートは、エンティティのフィールドに一致する構造を持つ Excel ファイルですが、データは含みません。 テンプレートをダウンロードした後、手動またはプログラムでデータを設定して、サービスにインポートして戻します。 エンティティ内の **[Export Template]** (テンプレートのエクスポート) をクリックして、必要なフィールドを指定します (ここではフィールドを 1 つ選択しました)。 **[Export to Excel]** (Excel にエクスポート) をクリックして、Excel ファイルが生成されるまで待ちます。 Excel ファイルを開いて、エクスポートしたテンプレートに選択したフィールドがあることを確認します。

![Excel にテンプレートをエクスポートする](./media/learning-common-data-service-manage/export-template.png)

## <a name="open-and-work-with-data-in-excel"></a>Excel でデータを開いて操作する
最後に、**[Open in Excel]** (Excel で開く) オプションを確認しましょう。 PowerApps アドインをインストールしてある場合は、このオプションを使用して Excel でデータを表示して編集することができます。 エンティティ内の **[Open in Excel]** (Excel で開く) をクリックして、ファイルを開きます。 編集を有効にすると、アドインによってサービスのエンティティとのライブ接続が確立されて、ブックにデータが表示されます。 ブック内で直接編集するので、行の追加や削除ができます。 **[Publish]** (発行) をクリックして変更を保存します。 データを更新して最新のコピーがあるかどうか確認することもできます。データをフィルター処理することもできます。フィルター処理は、エンティティ内に大量のデータがある場合に特に便利です。

![Excel で開く](./media/learning-common-data-service-manage/open-excel.png)

Common Data Service でのデータ管理に関するトピック (データのインポートとエクスポート、Excel での操作) は以上です。 次のトピックでは、データのセキュリティ管理について説明します。

