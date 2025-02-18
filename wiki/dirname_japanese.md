# [日本語] Debian Almquist Shell (dash) dirname 使用法: ファイルパスからディレクトリ名を取得する

## Overview
`dirname` コマンドは、指定されたファイルパスからディレクトリ名を抽出するためのコマンドです。このコマンドを使用することで、ファイルが存在するディレクトリのパスを簡単に取得できます。

## Usage
基本的な構文は以下の通りです。

```sh
dirname [options] [arguments]
```

## Common Options
- `-z`: 出力をヌル文字で区切ります。スクリプトでの処理に便利です。

## Common Examples
以下に、`dirname` コマンドのいくつかの実用的な例を示します。

### 例1: 基本的な使用法
ファイルパスからディレクトリ名を取得します。

```sh
dirname /home/user/documents/file.txt
```
出力:
```
/home/user/documents
```

### 例2: 相対パスの使用
相対パスを指定してディレクトリ名を取得します。

```sh
dirname ./projects/code/script.sh
```
出力:
```
./projects/code
```

### 例3: ヌル文字での出力
複数のファイルパスをヌル文字で区切って出力します。

```sh
dirname -z /home/user/documents/file1.txt /home/user/documents/file2.txt
```
出力:
```
/home/user/documents\0/home/user/documents
```

## Tips
- スクリプト内で使用する際は、出力を変数に格納して後続の処理に利用すると便利です。
- `dirname` コマンドは、ファイルパスの形式に依存するため、正しいパスを指定することが重要です。