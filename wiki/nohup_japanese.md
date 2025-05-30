# [日本語] Debian Almquist Shell (dash) nohup の使い方: プロセスを切り離して実行する

## 概要
`nohup` コマンドは、シェルセッションが終了してもプロセスを実行し続けるためのコマンドです。通常、シェルを閉じるとその中で実行されているプロセスも終了しますが、`nohup` を使うことで、プロセスをバックグラウンドで安全に実行できます。

## 使用法
基本的な構文は次の通りです。

```
nohup [オプション] [コマンド] [引数]
```

## 一般的なオプション
- `&` : コマンドをバックグラウンドで実行します。
- `-h` : ヘルプメッセージを表示します。
- `-v` : 詳細情報を表示します。

## 一般的な例
以下に、`nohup` コマンドのいくつかの実用的な例を示します。

### 例1: バックグラウンドでスクリプトを実行
```bash
nohup ./myscript.sh &
```

### 例2: ログファイルに出力をリダイレクト
```bash
nohup python myscript.py > output.log &
```

### 例3: プロセスの実行を確認
```bash
nohup sleep 60 &
```

## ヒント
- `nohup` を使用する際は、出力をリダイレクトすることをお勧めします。デフォルトでは、出力は `nohup.out` に保存されます。
- プロセスがバックグラウンドで実行されていることを確認するために、`jobs` コマンドを使用できます。
- 長時間実行するプロセスには、`nohup` を使用することで、シェルを閉じても影響を受けずに実行を続けることができます。