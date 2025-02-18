# [台灣] Debian Almquist Shell (dash) scp 使用方式: 複製檔案

## Overview
`scp`（Secure Copy Protocol）是一個用於在本地和遠端主機之間安全地複製檔案的命令。它利用SSH協議來加密傳輸過程，確保資料的安全性。

## Usage
基本語法如下：
```
scp [options] [source] [destination]
```

## Common Options
- `-r`: 遞迴複製整個目錄。
- `-P port`: 指定連接的端口號（注意是大寫的 P）。
- `-i identity_file`: 使用指定的身份驗證檔案。
- `-v`: 顯示詳細的運行過程，便於除錯。

## Common Examples
1. 複製本地檔案到遠端主機：
   ```bash
   scp localfile.txt user@remote_host:/path/to/destination/
   ```

2. 從遠端主機複製檔案到本地：
   ```bash
   scp user@remote_host:/path/to/remotefile.txt /local/destination/
   ```

3. 遞迴複製整個目錄到遠端主機：
   ```bash
   scp -r /local/directory user@remote_host:/path/to/destination/
   ```

4. 使用指定的端口號複製檔案：
   ```bash
   scp -P 2222 localfile.txt user@remote_host:/path/to/destination/
   ```

## Tips
- 確保SSH服務在遠端主機上運行，否則無法使用`scp`命令。
- 使用`-v`選項可以幫助你了解連接過程中的問題。
- 當複製大量檔案時，考慮使用`-C`選項來啟用壓縮，這樣可以加快傳輸速度。