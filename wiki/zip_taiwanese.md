# [台灣] Debian Almquist Shell (dash) zip 使用法: 壓縮檔案

## Overview
`zip` 命令用於將一個或多個檔案壓縮成一個壓縮檔案，通常以 `.zip` 為副檔名。這個命令不僅可以減少檔案的大小，還可以方便檔案的傳輸和儲存。

## Usage
基本語法如下：
```
zip [options] [arguments]
```

## Common Options
- `-r`：遞迴壓縮目錄及其內容。
- `-e`：加密壓縮檔案，需輸入密碼。
- `-d`：從壓縮檔案中刪除指定的檔案。
- `-u`：更新壓縮檔案中的檔案，僅壓縮較新的檔案。

## Common Examples
以下是一些常見的使用範例：

1. 壓縮單個檔案：
   ```sh
   zip myarchive.zip file1.txt
   ```

2. 壓縮多個檔案：
   ```sh
   zip myarchive.zip file1.txt file2.txt file3.txt
   ```

3. 遞迴壓縮整個目錄：
   ```sh
   zip -r myarchive.zip myfolder/
   ```

4. 更新壓縮檔案中的檔案：
   ```sh
   zip -u myarchive.zip file1.txt
   ```

5. 加密壓縮檔案：
   ```sh
   zip -e myarchive.zip file1.txt
   ```

## Tips
- 在壓縮大量檔案時，使用 `-r` 選項可以一次性壓縮整個目錄，節省時間。
- 使用加密選項時，請確保記住密碼，否則將無法解壓縮檔案。
- 定期更新壓縮檔案中的內容，保持檔案的最新狀態，有助於管理檔案。