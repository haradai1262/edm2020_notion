# edm2020_notion

EDM2020のProceedingsから論文リストを取得して、Notionページを作成する

- [EDM2020 Proceedings](https://educationaldatamining.org/edm2020/proceedings/)から論文のタイトル、著者、PDF URL、アブストラクトを取得
  - アブストラクトはダウンロードしたPDFから[pdfminer](https://www.unixuser.org/~euske/python/pdfminer/)により抽出 (3割ぐらいは失敗してる)
- [notion-py](https://github.com/jamalex/notion-py) を使用してNotionページを作成する
- 作成されるNotionページ: https://www.notion.so/myaun/EDM2020-proceedings-81c7b43901384889ab66943fb747f5b8

## Usage

- notion tokenを取得
  - 参考 [トークンの取得方法 / How to get your token](https://www.notion.so/How-to-get-your-token-d7a3421b851f406380fb9ff429cd5d47)
- 取得したtokenを[secrets/token_info.py]に以下のように記述
  - ```token_v2 = "hogehoge" ```
- [notebook/edm2020procs2notion.ipynb] を起動->実行