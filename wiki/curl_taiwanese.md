# [台灣] Debian Almquist Shell (dash) curl 使用方式: 用於傳輸資料的命令

## Overview
curl 是一個用於從或向伺服器傳輸資料的命令行工具。它支援多種協議，包括 HTTP、HTTPS、FTP 等，並且可以用來下載或上傳檔案。

## Usage
基本語法如下：
```bash
curl [options] [arguments]
```

## Common Options
- `-O`：將下載的檔案儲存為原始檔名。
- `-L`：自動跟隨重定向。
- `-d`：用於發送 POST 請求的資料。
- `-H`：添加自定義的 HTTP 標頭。
- `-u`：用於提供用戶名和密碼進行身份驗證。

## Common Examples
以下是一些常見的 curl 使用範例：

1. 下載檔案並儲存為原始檔名：
   ```bash
   curl -O http://example.com/file.zip
   ```

2. 自動跟隨重定向：
   ```bash
   curl -L http://example.com
   ```

3. 發送 POST 請求：
   ```bash
   curl -d "param1=value1&param2=value2" http://example.com/api
   ```

4. 添加自定義 HTTP 標頭：
   ```bash
   curl -H "Authorization: Bearer token" http://example.com/protected
   ```

5. 使用用戶名和密碼進行身份驗證：
   ```bash
   curl -u username:password http://example.com
   ```

## Tips
- 使用 `-I` 選項可以查看 HTTP 響應標頭，這對於調試非常有用。
- 結合 `-o` 選項來指定下載檔案的名稱，這樣可以避免使用原始檔名。
- 確保在使用敏感資訊（如密碼）時，使用 HTTPS 來保護資料安全。