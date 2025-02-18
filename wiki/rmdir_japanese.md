# [日本語] Debian Almquist Shell (dash) rmdir 使用法: 空のディレクトリを削除する

## Overview
`rmdir` コマンドは、空のディレクトリを削除するために使用されます。このコマンドは、指定されたディレクトリが空である場合にのみ成功します。

## Usage
基本的な構文は以下の通りです。

```bash
rmdir [オプション] [引数]
```

## Common Options
- `--ignore-fail-on-non-empty` : 空でないディレクトリが存在してもエラーを無視します。
- `--verbose` : 削除したディレクトリの詳細を表示します。

## Common Examples
以下は、`rmdir` コマンドのいくつかの実用的な例です。

### 例1: 空のディレクトリを削除する
```bash
rmdir /path/to/empty-directory
```

### 例2: 複数の空のディレクトリを削除する
```bash
rmdir /path/to/empty-directory1 /path/to/empty-directory2
```

### 例3: 削除の詳細を表示する
```bash
rmdir --verbose /path/to/empty-directory
```

### 例4: 空でないディレクトリを無視する
```bash
rmdir --ignore-fail-on-non-empty /path/to/non-empty-directory
```

## Tips
- `rmdir` を使用する前に、削除したいディレクトリが本当に空であることを確認してください。
- 複数のディレクトリを一度に削除する場合は、スペースで区切って指定できます。
- `rmdir` は、削除できないディレクトリに対してエラーメッセージを表示しますので、注意深く使用してください。