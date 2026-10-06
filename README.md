# AIEプレ講座 学習記録

講座で取り組むLinux・Git・DockerとWebアプリの演習をまとめたリポジトリです。講座の学習記録・演習コードとして位置付けています。

## 案内

| 内容 | ファイル |
| --- | --- |
| preDay 1の記録 | [records/pre_day1.md](records/pre_day1.md) |
| PRE-DAY2 | [docs/PRE-DAY2.md](docs/PRE-DAY2.md) |
| PRE-DAY3 | [docs/PRE-DAY3.md](docs/PRE-DAY3.md) |
| 環境準備スクリプト | [pre_day3/prepare.sh](pre_day3/prepare.sh) |
| Webアプリ演習の起動方法 | [lecture/README.md](lecture/README.md) |
| 次の課題 | [tasks.md](tasks.md) |

## 演習アプリの構成

React・TypeScriptの入力画面から、Nginxのリバースプロキシを経由してFastAPIへPOSTします。通常モードでは入力文字列の文字数を返し、mockモードでは固定の応答を返します。Docker Composeでフロントエンドとバックエンドを起動する構成です。

## 起動・確認

DockerとDocker Composeが必要です。lectureフォルダで.env.exampleを.envへコピーし、詳細な手順は[演習README](lecture/README.md)を参照してください。

```sh
cd lecture
cp backend/.env.example backend/.env
chmod 600 backend/.env
docker compose up -d --build
```

http://localhost:8080/ を開き、文字を入力して送信し、応答を確認します。今回Docker上での起動確認は未実施です。

## 学習内容を説明する観点

- ファイル権限と環境変数の扱い
- フロントエンド・API・プロキシの役割分担
- ブラウザから相対パスでAPIを呼ぶ理由
- HTTPエラーと通信失敗の区別

習得度や実行結果は記録した事実をもとに説明し、未確認の動作を実績として扱いません。
