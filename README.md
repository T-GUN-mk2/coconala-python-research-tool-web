# Web公開用フォルダ

このフォルダは、Cloudflare Pagesで公開するWebサイト用の作業場所です。

## 想定構成

- `index.html`: トップページ
- `works/index.html`: 東京大学研究室への導入実績とIR・XRD解析アプリ（`/works/`）
- `flow/index.html`: 開発の流れ、見積り方針、相談前の整理項目（`/flow/`）
- `faq/index.html`: よくある質問16項目（`/faq/`）
- `assets/css/`: CSSファイル
- `assets/js/`: JavaScriptファイル
- `assets/images/`: Webサイトで使う画像（IR・XRD解析アプリのサンプル動作画面を含む）
- `.demo/`: サンプルデータと画面生成用のローカル補助ファイル（Git公開対象外）

## Cloudflare Pages連携時の想定

- プロジェクトルート: リポジトリ直下（この`web`フォルダを独立リポジトリとして使用）
- ビルドコマンド: 静的HTMLなら未設定または不要
- 出力ディレクトリ: `.`

既存のココナラ出品用モックアップとは分けて、このフォルダ内に公開サイト用ファイルを作成していきます。

## 解析アプリ掲載画像

- `assets/images/ir-analyzer-demo.png`: 実装済みIR解析アプリへ生成サンプルデータを読み込んだ画面
- `assets/images/xrd-analyzer-demo.png`: 実装済みXRD解析アプリへ生成サンプルデータを読み込んだ画面
- 掲載値は実測データではなく、機能・表示確認用に生成したサンプルです
- 元のIR・XRD解析スクリプトや実験データは、この公開フォルダへコピーしていません

## 外部リンクの状態

- noteリンクは `https://note.com/okonomitgn_` に接続済み
- ココナラ出品ページURLは未確定のため、無料相談ボタンと仮導線は表示しない
- ココナラURL確定後は、設置場所と文言を決めてから `target="_blank" rel="noopener"` 付きで追加する
- 独自ドメイン公開後、必要に応じてOGP画像URLやサイトマップを絶対URLで設定する

## Cloudflare Pages用ファイル

- `_headers`: セキュリティヘッダーと静的アセットのキャッシュ設定
- `robots.txt`: 検索エンジン向けのクロール許可
- `404.html`: 存在しないURLにアクセスした場合の簡易ページ
