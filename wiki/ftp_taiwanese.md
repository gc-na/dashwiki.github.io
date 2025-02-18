# [台灣] Debian Almquist Shell (dash) ftp 使用法: 用於檔案傳輸的命令

## Overview
`ftp` 命令用於在客戶端和伺服器之間傳輸檔案。它支持多種檔案傳輸操作，包括上傳和下載檔案。

## Usage
基本語法如下：
```
ftp [options] [arguments]
```

## Common Options
- `-i`: 取消交互模式，適合批次傳輸。
- `-n`: 不自動登入，適合需要手動登入的情況。
- `-v`: 顯示詳細的傳輸過程。

## Common Examples
以下是一些常見的 `ftp` 使用範例：

1. 連接到 FTP 伺服器：
   ```sh
   ftp ftp.example.com
   ```

2. 使用匿名登入：
   ```sh
   ftp -n ftp.example.com
   ```

3. 上傳檔案：
   ```sh
   put localfile.txt
   ```

4. 下載檔案：
   ```sh
   get remotefile.txt
   ```

5. 列出伺服器上的檔案：
   ```sh
   ls
   ```

## Tips
- 確保在使用 `ftp` 時，伺服器的防火牆允許 FTP 連接。
- 使用 `-i` 選項可加快大量檔案的傳輸速度。
- 在傳輸敏感資料時，考慮使用更安全的 SFTP 或 FTPS。