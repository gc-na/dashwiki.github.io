# [日本語] Debian Almquist Shell (dash) nslookup の使い方: DNS情報を照会する

## 概要
`nslookup` コマンドは、DNS（ドメインネームシステム）サーバーに問い合わせを行い、ドメイン名に関連する情報を取得するためのツールです。これにより、IPアドレスやドメイン名の解決が可能になります。

## 使用法
基本的な構文は以下の通りです。

```bash
nslookup [オプション] [引数]
```

## 一般的なオプション
- `-type=TYPE` : 照会するレコードのタイプを指定します（例：A、MX、CNAMEなど）。
- `-timeout=秒数` : タイムアウト時間を指定します。
- `-retry=回数` : 再試行の回数を指定します。

## 一般的な例
以下に、`nslookup` コマンドのいくつかの実用的な例を示します。

### 1. ドメイン名からIPアドレスを取得
```bash
nslookup example.com
```

### 2. 特定のDNSサーバーを使用して照会
```bash
nslookup example.com 8.8.8.8
```

### 3. MXレコードを取得
```bash
nslookup -type=MX example.com
```

### 4. CNAMEレコードを取得
```bash
nslookup -type=CNAME www.example.com
```

## ヒント
- `nslookup` を使用する際は、特定のDNSサーバーを指定することで、異なる結果を得られることがあります。
- 結果が正確でない場合は、DNSキャッシュをクリアして再試行してください。
- `nslookup` は対話モードでも使用可能で、複数の照会を行うことができます。対話モードに入るには、単に `nslookup` と入力してください。