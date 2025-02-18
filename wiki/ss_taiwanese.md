# [台灣] Debian Almquist Shell (dash) ss 使用法: 檢視網路連線狀態

## Overview
`ss` 命令用於顯示網路連線的狀態，提供有關 TCP、UDP 及其他網路協定的詳細資訊。它是用來替代 `netstat` 的一個工具，能夠更快速地顯示網路連線的狀態。

## Usage
基本語法如下：
```
ss [options] [arguments]
```

## Common Options
- `-t`: 顯示 TCP 連線。
- `-u`: 顯示 UDP 連線。
- `-l`: 顯示正在監聽的連線。
- `-p`: 顯示使用該連線的程序。
- `-n`: 以數字格式顯示地址和端口號，避免 DNS 查詢。

## Common Examples
1. 顯示所有 TCP 連線：
   ```bash
   ss -t
   ```

2. 顯示所有 UDP 連線：
   ```bash
   ss -u
   ```

3. 顯示所有正在監聽的連線：
   ```bash
   ss -l
   ```

4. 顯示所有連線及其使用的程序：
   ```bash
   ss -p
   ```

5. 以數字格式顯示所有 TCP 連線：
   ```bash
   ss -tn
   ```

## Tips
- 使用 `ss` 時，可以結合多個選項以獲取更精確的資訊，例如 `ss -tunlp` 會顯示所有的 TCP 和 UDP 連線及其程序。
- 若要定期檢查網路狀態，可以將 `ss` 命令放入一個簡單的腳本中，並使用 `watch` 命令來定期執行。
- 注意 `ss` 的輸出可能會因系統的不同而有所變化，建議在不同環境中多加測試。