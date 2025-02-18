# [日本語] Debian Almquist Shell (dash) shift の使い方: 引数を左にシフトする

## 概要
`shift` コマンドは、シェルスクリプト内で位置パラメータを左にシフトするために使用されます。これにより、スクリプト内の引数を簡単に操作することができます。

## 使用法
基本的な構文は以下の通りです。

```
shift [n]
```

ここで、`n` はシフトする位置パラメータの数を指定します。指定しない場合は、デフォルトで1つシフトします。

## 一般的なオプション
- `n` : シフトする位置パラメータの数を指定します。省略すると1つシフトします。

## 一般的な例
以下は、`shift` コマンドの実用的な例です。

### 例1: デフォルトのシフト
```sh
#!/bin/dash
set -- arg1 arg2 arg3
echo "Before shift: $1"  # 出力: arg1
shift
echo "After shift: $1"   # 出力: arg2
```

### 例2: 複数の引数をシフト
```sh
#!/bin/dash
set -- one two three four
echo "Before shift: $1"  # 出力: one
shift 2
echo "After shift: $1"   # 出力: three
```

### 例3: 引数の確認
```sh
#!/bin/dash
set -- apple banana cherry
while [ "$#" -gt 0 ]; do
  echo "Current argument: $1"
  shift
done
```

## ヒント
- `shift` コマンドは、引数の処理を簡素化するために非常に便利です。特にループ内で使用することで、引数を一つずつ処理できます。
- 引数の数を確認するために、`$#` を使用して残りの引数の数をチェックすることができます。
- スクリプトの可読性を向上させるために、`shift` を使用する際は、コメントを追加してシフトの目的を明確にしましょう。