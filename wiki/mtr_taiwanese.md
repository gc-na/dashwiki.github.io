# [台灣] Debian Almquist Shell (dash) mtr 使用法: 網路路徑追蹤工具

## Overview
mtr（My Traceroute）是一個結合了 traceroute 和 ping 功能的網路診斷工具。它可以幫助使用者追蹤資料包在網路中的路徑，並顯示每一跳的延遲和丟包率，從而協助找出網路問題。

## Usage
基本語法如下：
```bash
mtr [options] [arguments]
```

## Common Options
- `-r`：以報告模式運行，輸出一次性報告。
- `-c <count>`：指定要發送的請求數量。
- `-i <interval>`：設置發送請求的間隔時間（秒）。
- `-p`：顯示每一跳的端口號。
- `-w`：以寬格式輸出結果。

## Common Examples
以下是一些常見的 mtr 使用範例：

1. 基本使用：
   ```bash
   mtr google.com
   ```

2. 以報告模式運行，並發送 10 次請求：
   ```bash
   mtr -r -c 10 google.com
   ```

3. 設定請求間隔為 1 秒：
   ```bash
   mtr -i 1 google.com
   ```

4. 顯示端口號：
   ```bash
   mtr -p google.com
   ```

5. 以寬格式輸出結果：
   ```bash
   mtr -w google.com
   ```

## Tips
- 在進行網路故障排除時，使用 `-r` 選項可以快速獲得一次性的報告，方便分析。
- 嘗試不同的 `-c` 和 `-i` 值來調整測試的頻率和持續時間，以獲得更準確的結果。
- 當追蹤特定的伺服器時，確保該伺服器允許 ICMP 請求，否則可能會得到不完整的結果。