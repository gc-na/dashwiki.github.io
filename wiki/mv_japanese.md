# [日本語] Debian Almquist Shell (dash) mv の使い方: ファイルやディレクトリの移動と名前変更

## Overview
`mv` コマンドは、ファイルやディレクトリを移動したり、名前を変更したりするために使用されます。このコマンドを使うことで、ファイルシステム内のファイルの位置を簡単に変更できます。

## Usage
基本的な構文は以下の通りです。

```bash
mv [options] [source] [destination]
```

## Common Options
- `-i`: 上書きする前に確認を求める。
- `-u`: 既存のファイルよりも新しい場合のみ移動する。
- `-v`: 実行中の操作を表示する。

## Common Examples
以下に、`mv` コマンドのいくつかの実用的な例を示します。

### ファイルの移動
特定のファイルを別のディレクトリに移動する場合：

```bash
mv example.txt /home/user/documents/
```

### ファイルの名前変更
ファイルの名前を変更する場合：

```bash
mv oldname.txt newname.txt
```

### 複数ファイルの移動
複数のファイルを一度に移動する場合：

```bash
mv file1.txt file2.txt /home/user/documents/
```

### 上書き確認
上書きする前に確認を求める場合：

```bash
mv -i example.txt /home/user/documents/
```

## Tips
- 移動先のディレクトリが存在するか確認してから実行すると、エラーを避けられます。
- `-v` オプションを使用すると、どのファイルが移動されたかを確認できるので、特に複数のファイルを扱う場合に便利です。
- 名前変更を行う際は、ファイルの拡張子を確認して、意図した形式であることを確認しましょう。