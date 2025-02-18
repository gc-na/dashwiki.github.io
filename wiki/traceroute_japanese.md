# [日本語] Debian Almquist Shell (dash) traceroute の使い方: ネットワーク経路の追跡

## Overview
`traceroute` コマンドは、指定したホストまでのネットワーク経路を追跡し、各中継点の応答時間を測定するために使用されます。これにより、ネットワークの遅延や障害の原因を特定するのに役立ちます。

## Usage
基本的な構文は以下の通りです。

```
traceroute [options] [arguments]
```

## Common Options
- `-m <max_ttl>`: 最大TTL（Time To Live）値を指定します。
- `-n`: ホスト名の解決を行わず、IPアドレスのみを表示します。
- `-p <port>`: 使用するポート番号を指定します。
- `-q <nqueries>`: 各ホップに対して送信するクエリの数を指定します。

## Common Examples
以下は、`traceroute` コマンドのいくつかの実用的な例です。

### 基本的な使用法
特定のホストへの経路を追跡する基本的なコマンドです。
```bash
traceroute example.com
```

### 最大TTLを指定する
最大TTLを15に設定して経路を追跡します。
```bash
traceroute -m 15 example.com
```

### IPアドレスのみを表示
ホスト名の解決を行わず、IPアドレスのみを表示します。
```bash
traceroute -n example.com
```

### 特定のポートを使用
特定のポート（例：80）を使用して経路を追跡します。
```bash
traceroute -p 80 example.com
```

## Tips
- `traceroute` を使用する際は、ネットワークの遅延や問題を特定するために、複数回実行して結果を比較することをお勧めします。
- 経路の途中で応答しないホップがある場合、それは必ずしも問題ではなく、特定のルーターがICMPパケットを無視している可能性があります。
- `-n` オプションを使用することで、結果の表示が速くなり、特に多くのホップがある場合に便利です。