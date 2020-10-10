# simple-git-cli

## インストール

```bash
$ npm install -g simple-git-cli
```

## 使い方

### 事前準備

事前準備は、プロジェクトフォルダにつき1回実行してください。

```bash
$ sgit create <プロジェクト名>
```

例

```bash
$ cd /path/to/project/folder
$ sgit create sample-project
準備を開始します。
GitHubのユーザー名/メールアドレスを入力してください。
> {ここにユーザー名を入力してください}
GitHubのパスワードを入力してください。
> {ここにパスワードを入力してください}
準備しています...
準備が完了しました。以下のURLからアップロードしたファイルを見ることができます。
  https://github.com/{ユーザー名}/sample-project

新しいファイルをアップロードする場合は、以下のコマンドを実行してください。
  $ sgit upload
```

同じプロジェクトフォルダに`create`コマンドを複数回実行した場合、以下のメッセージが表示されます。

```bash
$ sgit create sample-project
このフォルダは準備済みです。
```

リポジトリはデフォルトでプライベートで作成されます。

### GitHubにコードをアップロードする

```bash
$ sgit upload
```

省略コマンド
```bash
$ sgit up
```

例
```bash
$ sgit upload
ファイルをアップロードしています...
アップロードが完了しました。
```

内部的には以下のコマンドを実行しています。

```bash
$ git add .
$ git commit -m "{現在時刻}"
$ git push
```
