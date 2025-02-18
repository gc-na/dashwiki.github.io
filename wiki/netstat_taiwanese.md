# [台灣] Debian Almquist Shell (dash) netstat 使用方式: 檢查網路連接狀態

## Overview
`netstat` 是一個用於顯示網路連接、路由表、介面統計以及網路協定等資訊的命令。它可以幫助使用者了解系統的網路狀態，並進行故障排除。

## Usage
基本語法如下：
```
netstat [options] [arguments]
```

## Common Options
- `-a`：顯示所有連接和監聽的端口。
- `-n`：以數字形式顯示地址和端口號，而不是解析為主機名。
- `-t`：顯示 TCP 連接。
- `-u`：顯示 UDP 連接。
- `-l`：僅顯示正在監聽的服務。
- `-p`：顯示使用每個連接的程序識別碼 (PID) 和程序名稱。

## Common Examples
1. 顯示所有連接和監聽的端口：
   ```bash
   netstat -a
   ```

2. 以數字形式顯示所有 TCP 連接：
   ```bash
   netstat -tn
   ```

3. 顯示所有 UDP 連接：
   ```bash
   netstat -un
   ```

4. 顯示正在監聽的服務及其程序：
   ```bash
   netstat -lp
   ```

5. 顯示路由表：
   ```bash
   netstat -r
   ```

## Tips
- 使用 `-n` 選項可以加快命令執行速度，因為它不會進行 DNS 查詢。
- 結合 `grep` 命令可以過濾特定的連接，例如：
  ```bash
  netstat -an | grep LISTEN
  ```
- 定期檢查網路連接狀態可以幫助及早發現潛在的問題。