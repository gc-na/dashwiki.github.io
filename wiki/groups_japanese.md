# [日本語] Debian Almquist Shell (dash) groups の使い方: ユーザーのグループを表示する

## Overview
`groups` コマンドは、指定されたユーザーが所属しているグループを表示します。引数を指定しない場合は、現在のユーザーのグループを表示します。

## Usage
基本的な構文は以下の通りです。

```
groups [options] [arguments]
```

## Common Options
- `-h`, `--help`: ヘルプメッセージを表示します。
- `-V`, `--version`: バージョン情報を表示します。

## Common Examples
以下に、`groups` コマンドの実用的な例を示します。

### 現在のユーザーのグループを表示
```bash
groups
```

### 特定のユーザーのグループを表示
```bash
groups username
```

### 複数のユーザーのグループを表示
```bash
groups user1 user2
```

## Tips
- `groups` コマンドは、ユーザーのグループ情報を確認するのに便利です。特に、アクセス権のトラブルシューティングに役立ちます。
- グループの変更や追加を行う前に、現在のグループを確認しておくと良いでしょう。