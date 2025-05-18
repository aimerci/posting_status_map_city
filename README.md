## posting_status_map

<br>

- 市区町村単位（市区町村コード）を元に、Excel上の枚数データを、地図上に可視化します

<br>

## 準備

### データの取得
- Google Form で情報を取得します
- Google Spreadsheet で集計やキーコードとの紐づけを行います  
  - キーコードは行政コードがおすすめ  
  - 公開設定に注意。別スプシを作成し、IMPORTRANGE関数がおすすめ
  - [解説ページ](https://roboma.io/blog/marketing/importrange-function-of-google-spreadsheet/)

### Github更新
- Google Spreadsheet からデータを CSVファイルで保存する
- data フォルダに CSVファイルをアップロードする
- index.html内の、ファイルパスを確認・更新する
- index.html内の、キーコードを確認・更新する

