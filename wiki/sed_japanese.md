# [日本語] Debian Almquist Shell (dash) sed 使用法: テキストの変換と編集

## Overview
`sed`は、ストリームエディタとして知られ、テキストデータを処理し、変換するための強力なツールです。主にファイルの内容を変更したり、特定のパターンに基づいてテキストを編集するのに使用されます。

## Usage
基本的な構文は次の通りです。

```bash
sed [options] [arguments]
```

## Common Options
- `-e`: 複数の編集コマンドを指定するために使用します。
- `-i`: ファイルを直接編集します（バックアップを作成するオプションも指定可能）。
- `-n`: 出力を抑制し、特定の行だけを表示します。
- `s/pattern/replacement/`: 指定したパターンを置換します。

## Common Examples
以下は、`sed`の一般的な使用例です。

### 1. テキストの置換
ファイル内の「apple」を「orange」に置き換えます。

```bash
sed 's/apple/orange/' filename.txt
```

### 2. ファイルを直接編集
ファイル内の「apple」を「orange」に置き換え、変更をファイルに保存します。

```bash
sed -i 's/apple/orange/' filename.txt
```

### 3. 特定の行を表示
ファイルの2行目だけを表示します。

```bash
sed -n '2p' filename.txt
```

### 4. 複数の置換を行う
ファイル内の「apple」を「orange」に、そして「banana」を「grape」に置き換えます。

```bash
sed -e 's/apple/orange/' -e 's/banana/grape/' filename.txt
```

## Tips
- `-i`オプションを使用する際は、必ずバックアップを取ることをお勧めします。
- `sed`の正規表現を活用することで、より複雑なパターンマッチングが可能です。
- スクリプト内で`sed`を使用する場合、シングルクォートを使ってコマンドを囲むと、変数展開を防げます。