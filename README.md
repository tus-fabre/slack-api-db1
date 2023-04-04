# slack-api-db1

## NodeJSとSlack APIによるいまどきのネットワークプログラミング

### データベースにアクセスする その1

Slackからデータベースに接続して、その内容を画面に反映する。そのため、データベースの基本操作とNode.jsから接続する方法を学ぶ。用いるデータベースは世界約200ヶ国の国名を英語表記と日本語表記の両方で表現する。利用するWebサービスは海外のサイトであり、すべて英語で情報が返ってくるのでそれを日本語化するために用いる。

[動作確認の手順]

1. スラッシュコマンド/translateがSlackアプリに定義されているか確認する
1. コマンドプロンプトを開き、ダウンロードしたフォルダへ移動する
1. npm installコマンドでアプリに依存するパッケージをインストールする
1. .envファイルの環境変数SLACK_BOT_TOKENとSLACK_APP_TOKENに作成したSlackアプリのBotユーザートークンとアプリトークンが設定されていることを確認する
1. .envファイルの環境変数DB_URLがインストールしたPostgreSQLのユーザー名、パスワード、ポート番号に設定されていることを確認する
    postgres://<ユーザー名>:<パスワード>@<サーバー名>:<ポート番号>/<データベース名>
1. アプリを起動する
    $ node ./app.js
1. Slackアプリをインストールしたチャネルを開く
1. メッセージ欄に「/translate <英語国名>」と入力し、送信する
    例：/translate USA
1. 日本語名に変換されることを確認する
