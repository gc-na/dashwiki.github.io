# [日本語] Debian Almquist Shell (dash) scp 使用法: リモートファイル転送

## 概要
`scp` コマンドは、SSH（Secure Shell）を使用して、ローカルとリモートの間でファイルを安全に転送するためのコマンドです。このコマンドを使用することで、ネットワーク越しにファイルを簡単にコピーできます。

## 使用法
基本的な構文は以下の通りです。

```bash
scp [オプション] [元ファイル] [ユーザー名@ホスト名:宛先パス]
```

## 一般的なオプション
- `-r`: ディレクトリを再帰的にコピーします。
- `-P`: SSHポートを指定します（大文字のP）。
- `-i`: 特定のSSH鍵ファイルを指定します。
- `-v`: 詳細な出力を表示します（デバッグ用）。

## 一般的な例
以下に、`scp` コマンドのいくつかの実用的な例を示します。

### 1. ローカルファイルをリモートサーバーにコピー
```bash
scp /path/to/local/file.txt username@remote_host:/path/to/remote/directory/
```

### 2. リモートサーバーからローカルにファイルをコピー
```bash
scp username@remote_host:/path/to/remote/file.txt /path/to/local/directory/
```

### 3. ディレクトリを再帰的にコピー
```bash
scp -r /path/to/local/directory username@remote_host:/path/to/remote/directory/
```

### 4. 特定のポートを使用してコピー
```bash
scp -P 2222 /path/to/local/file.txt username@remote_host:/path/to/remote/directory/
```

## ヒント
- 転送するファイルが大きい場合は、`-C` オプションを使用して圧縮を有効にすると、転送速度が向上します。
- SSH鍵を使用して認証を行うことで、パスワードを入力せずにファイルを転送できます。
- `-v` オプションを使って、問題が発生した場合のデバッグ情報を得ることができます。