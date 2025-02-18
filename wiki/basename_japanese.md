# [日本語] Debian Almquist Shell (dash) basename 使用法: ファイル名の取得

## Overview
`basename` コマンドは、指定されたパスからファイル名を抽出するために使用されます。このコマンドは、ファイルの拡張子を取り除くことも可能です。

## Usage
基本的な構文は以下の通りです。

```bash
basename [options] [arguments]
```

## Common Options
- `-a`: 複数の引数を処理し、それぞれのベース名を出力します。
- `-s`: 指定されたサフィックスをファイル名から削除します。

## Common Examples
以下に、`basename` コマンドのいくつかの実用的な例を示します。

1. 単一のファイル名を取得する:
   ```bash
   basename /path/to/file.txt
   ```
   出力:
   ```
   file.txt
   ```

2. 拡張子を取り除いたファイル名を取得する:
   ```bash
   basename /path/to/file.txt .txt
   ```
   出力:
   ```
   file
   ```

3. 複数のファイル名を一度に取得する:
   ```bash
   basename -a /path/to/file1.txt /path/to/file2.txt
   ```
   出力:
   ```
   file1.txt
   file2.txt
   ```

4. 拡張子を取り除いた複数のファイル名を取得する:
   ```bash
   basename -a /path/to/file1.txt /path/to/file2.txt .txt
   ```
   出力:
   ```
   file1
   file2
   ```

## Tips
- `basename` コマンドは、スクリプト内でファイル名を処理する際に非常に便利です。
- 複数のファイルを処理する場合は、`-a` オプションを使用すると効率的です。
- 拡張子を取り除く際には、正確なサフィックスを指定することが重要です。