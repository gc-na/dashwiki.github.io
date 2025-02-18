# [台灣] Debian Almquist Shell (dash) ping6 使用法: 測試 IPv6 網路連通性

## Overview
`ping6` 是一個用於測試 IPv6 網路連通性的命令。它可以幫助用戶檢查與特定 IPv6 位址之間的連接是否正常，並提供延遲和丟包的資訊。

## Usage
基本語法如下：
```bash
ping6 [選項] [參數]
```

## Common Options
- `-c <count>`: 指定要發送的回應請求數量。
- `-i <interval>`: 設定發送請求的間隔時間（以秒為單位）。
- `-s <size>`: 設定每個請求的數據包大小（以位元組為單位）。
- `-W <timeout>`: 設定等待回應的超時時間（以秒為單位）。

## Common Examples
以下是一些常見的使用範例：

1. **基本的 ping6 測試**
   ```bash
   ping6 google.com
   ```

2. **發送 5 個請求**
   ```bash
   ping6 -c 5 google.com
   ```

3. **每 2 秒發送一次請求**
   ```bash
   ping6 -i 2 google.com
   ```

4. **設定數據包大小為 1280 位元組**
   ```bash
   ping6 -s 1280 google.com
   ```

5. **設定超時為 3 秒**
   ```bash
   ping6 -W 3 google.com
   ```

## Tips
- 在測試連接時，確保目標主機支援 IPv6。
- 使用 `-c` 選項可以避免無限迴圈，方便進行快速測試。
- 監控延遲和丟包率，這可以幫助你診斷網路問題。