# [台灣] Debian Almquist Shell (dash) sftp 使用方式: 用於安全文件傳輸

## Overview
sftp（SSH File Transfer Protocol）是一種安全的文件傳輸協議，允許用戶通過加密的連接在本地和遠程系統之間傳輸文件。它提供了比傳統的ftp更高的安全性，因為所有的數據都會被加密。

## Usage
基本的命令語法如下：
```
sftp [options] [user@]host
```

## Common Options
- `-b batchfile`：指定一個批處理文件，該文件包含要執行的sftp命令。
- `-C`：啟用壓縮，這可以加快傳輸速度。
- `-i identity_file`：指定用於身份驗證的私鑰文件。
- `-P port`：指定連接的端口號，默認為22。

## Common Examples
以下是一些常見的sftp使用範例：

1. 連接到遠程主機：
   ```bash
   sftp user@hostname
   ```

2. 上傳文件到遠程主機：
   ```bash
   sftp user@hostname
   put localfile.txt
   ```

3. 從遠程主機下載文件：
   ```bash
   sftp user@hostname
   get remotefile.txt
   ```

4. 使用批處理文件執行多個命令：
   ```bash
   sftp -b batchfile.txt user@hostname
   ```

5. 啟用壓縮進行傳輸：
   ```bash
   sftp -C user@hostname
   ```

## Tips
- 確保使用強密碼或密鑰來提高安全性。
- 使用批處理文件來自動化重複的文件傳輸任務。
- 在進行大文件傳輸時，考慮使用壓縮選項以提高效率。