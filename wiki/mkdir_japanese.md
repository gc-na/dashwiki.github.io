# [日本語] Debian Almquist Shell (dash) mkdir 使用法: ディレクトリを作成する

## Overview
`mkdir` コマンドは、新しいディレクトリを作成するために使用されます。このコマンドを使うことで、指定した名前のディレクトリをファイルシステム上に作成することができます。

## Usage
基本的な構文は以下の通りです。

```
mkdir [options] [arguments]
```

## Common Options
- `-p`: 親ディレクトリが存在しない場合でも、必要な親ディレクトリをすべて作成します。
- `-m`: 新しく作成するディレクトリのパーミッションを指定します。

## Common Examples
以下に、`mkdir` コマンドのいくつかの実用的な例を示します。

### 1. 単純なディレクトリの作成
```bash
mkdir my_directory
```

### 2. 複数のディレクトリを一度に作成
```bash
mkdir dir1 dir2 dir3
```

### 3. 親ディレクトリを含むディレクトリの作成
```bash
mkdir -p parent_dir/child_dir
```

### 4. 特定のパーミッションでディレクトリを作成
```bash
mkdir -m 755 my_secure_directory
```

## Tips
- ディレクトリ名にスペースを含める場合は、引用符で囲むことを忘れないでください。例: `mkdir "my directory"`
- `-p` オプションを使用すると、複数の階層を一度に作成できるため便利です。
- 作成したディレクトリのパーミッションを確認するには、`ls -ld directory_name` コマンドを使用してください。