# [台灣] Debian Almquist Shell (dash) traceroute 用法: 路徑追蹤工具

## Overview
`traceroute` 命令用於顯示從本地計算機到目標主機的路由路徑。它可以幫助用戶了解數據包在網絡中傳輸的過程，並識別可能的延遲或故障點。

## Usage
基本語法如下：
```
traceroute [options] [arguments]
```

## Common Options
- `-m <max_ttl>`: 設定最大生存時間（TTL），預設為30。
- `-n`: 直接使用IP地址，而不進行DNS查詢。
- `-p <port>`: 指定要使用的端口號，預設為33434。
- `-w <timeout>`: 設定每個回應的超時時間，預設為5秒。

## Common Examples
以下是一些常見的 `traceroute` 使用範例：

1. 基本用法，追蹤到某個主機：
   ```bash
   traceroute example.com
   ```

2. 使用IP地址而不進行DNS查詢：
   ```bash
   traceroute -n 8.8.8.8
   ```

3. 設定最大TTL為20：
   ```bash
   traceroute -m 20 example.com
   ```

4. 指定端口號為80：
   ```bash
   traceroute -p 80 example.com
   ```

5. 設定每個回應的超時時間為2秒：
   ```bash
   traceroute -w 2 example.com
   ```

## Tips
- 在進行故障排除時，使用 `-n` 選項可以加快結果顯示速度，因為它跳過DNS查詢。
- 如果你發現某個跳點的延遲異常，可以進一步使用 `ping` 命令檢查該跳點的狀態。
- 在大型網絡中，考慮減少最大TTL，以避免不必要的跳點顯示。