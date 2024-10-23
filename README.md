![見出しを追加](https://github.com/user-attachments/assets/24fe0ca1-9f89-41f2-a70a-8f4de6b0d778)

## このプロジェクトについて
SeleniumまたはRequestsを使用して**投票ページから各候補の投票数を取得し、Excelファイルに保存する**Pythonスクリプトです。

このスクリプトは、以下のYouTube動画で行われた投票のために作成されました:
>[【衝撃】Google検索では絶対に出てこない隠れた便利・暇つぶしサービス](https://www.youtube.com/watch?v=eqyAmSYw-p8&t=131s)

そのため、一部の機能または変数がその投票に適正化されています。  
使用する場合は、それらを適切な内容に変更してお使いください。

## 必要条件

- Python 3.x
- ChromeDriver (オプションです)
- 必要なPythonライブラリ（以下のインストール手順を参照）

## インストール

1. Python 3.x をインストールします。
2. ChromeDriver をダウンロードし、プロジェクトディレクトリに配置します。 (オプションです)
3. 必要なPythonライブラリをインストールします。

    ```sh
    pip install selenium openpyxl requests
    ```

## 使用方法

1. `main.py`もしくは`fullrequest.py`を実行します：

    ```sh
    python main.py
    ```
    ```sh
    python fullrequest.py
    ```

2. スクリプトは投票ページにアクセスし、特定の画像をクリックしてデータを取得します。
3. データは `project_votes.xlsx` という名前のExcelファイルに保存されます。

> [!TIP]
> `main.py`ではSeleniumが、`fullrequest.py`ではRequestsが使用されています。
> Requestsの方が処理は早いらしいですがNyaShinn1204さんが作成してくださったスクリプトなので詳しくは不明です。

## ファイル構成

- `main.py`: メインのPythonスクリプト
- `fullrequest.py`: 試験的なPythonスクリプト
- `chromedriver.exe`: ChromeDriver実行ファイル
- `project_votes.xlsx`: データが保存されるExcelファイル（スクリプト実行後に生成されます）

## ログ

スクリプトの実行中に発生するイベントやエラーは、コンソールにログとして出力されます。

## 注意事項

- ChromeDriverのバージョンは、インストールされているGoogle Chromeのバージョンと一致している必要があります。
- ウェブページの構造が変更された場合、スクリプトが正しく動作しない可能性があります。その場合は、XPathやその他のセレクタを更新してください。
- このスクリプトではスクレイピングを使用しています。リクエストの頻度を調整し、サーバーに過度な負荷をかけないようにしてください。
