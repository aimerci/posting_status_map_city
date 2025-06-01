## posting_status_map

<br>

- 市区町村単位（市区町村コード）を元に、Excel上の枚数データを、地図上に可視化します
- [地図ページ](https://aimerci.github.io/posting_status_map/view/)

<br>

## 準備

### データの取得
- Google Form で情報を取得します
- Google Spreadsheet で集計やキーコードとの紐づけを行います  
  - キーコードは行政コードがおすすめ  
  - 公開設定に注意。別スプシを作成し、IMPORTRANGE関数がおすすめ。[解説ページ](https://roboma.io/blog/marketing/importrange-function-of-google-spreadsheet/)

### Github更新
- Google Spreadsheet からデータを CSVファイルで保存する
- data フォルダに CSVファイルをアップロードする
- index.html内の、dataとgeojsonのファイルパスを確認・更新する
- index.html内の、キーコードを確認・更新する

<br>

## ロジック

- Google フォームを作る
- Google フォーム内で、郵便番号〜都道府県名〜市区町村名などを変換（GAS利用）
- Google フォームの回答スプレッドシート（非公開）に、集計シート（非公開）を追加
- 必要な単位で SUMIF を行い集計を実行する（非公開）
- 集計シートを別のスプレッドシートに IMPORTRANGE で引用する（公開シート）
- 集計公開シートのキーコードと、geojsonのキーコードを紐づけて、色塗りを行う
