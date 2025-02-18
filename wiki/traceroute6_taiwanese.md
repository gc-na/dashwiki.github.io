# [台灣] Debian Almquist Shell (dash) traceroute6 使用法: 網路路徑追蹤

## Overview
`traceroute6` 命令用於追蹤 IPv6 網路封包的路徑，幫助使用者了解數據如何從一個主機到達另一個主機。這個工具可以顯示經過的路由器及其延遲時間，對於網路故障排除非常有用。

## Usage
基本的語法如下：
```bash
traceroute6 [options] [arguments]
```

## Common Options
- `-m <max_ttl>`: 設定最大的生存時間（TTL），預設為 30。
- `-p <port>`: 指定要使用的端口號，預設為 33434。
- `-n`: 直接使用 IP 地址，而不解析主機名稱。
- `-w <timeout>`: 設定每個回應的超時時間，預設為 5 秒。

## Common Examples
以下是一些常見的使用範例：

1. 追蹤到特定的 IPv6 地址：
   ```bash
   traceroute6 2001:db8::1
   ```

2. 使用最大 TTL 設定為 20：
   ```bash
   traceroute6 -m 20 2001:db8::1
   ```

3. 使用指定的端口號：
   ```bash
   traceroute6 -p 80 2001:db8::1
   ```

4. 直接使用 IP 地址而不解析：
   ```bash
   traceroute6 -n 2001:db8::1
   ```

## Tips
- 在進行網路故障排除時，使用 `-n` 選項可以加快結果顯示，因為不需要進行 DNS 查詢。
- 嘗試不同的 TTL 值來查看路由的變化，這有助於識別網路瓶頸。
- 使用 `-w` 選項來調整超時時間，特別是在網路延遲較高的情況下。