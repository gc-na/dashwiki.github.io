# [台灣] Debian Almquist Shell (dash) basename 使用法: 獲取檔案名稱

## Overview
`basename` 命令用於從完整的檔案路徑中提取檔案名稱，並可選擇性地刪除檔案擴展名。這在處理檔案時非常有用，特別是當你只需要檔名而不需要完整路徑時。

## Usage
基本語法如下：
```
basename [options] [arguments]
```

## Common Options
- `-a`：處理多個檔案路徑，返回每個檔案的名稱。
- `-s`：指定要刪除的檔案擴展名。

## Common Examples
以下是一些常見的使用範例：

1. 獲取單一檔案的名稱：
   ```sh
   basename /usr/local/bin/script.sh
   ```
   輸出：
   ```
   script.sh
   ```

2. 獲取檔案名稱並刪除擴展名：
   ```sh
   basename /usr/local/bin/script.sh .sh
   ```
   輸出：
   ```
   script
   ```

3. 處理多個檔案路徑：
   ```sh
   basename -a /usr/local/bin/script.sh /home/user/file.txt
   ```
   輸出：
   ```
   script.sh
   file.txt
   ```

4. 獲取檔案名稱並刪除不同的擴展名：
   ```sh
   basename /path/to/archive.tar.gz .tar.gz
   ```
   輸出：
   ```
   archive
   ```

## Tips
- 當需要處理多個檔案時，使用 `-a` 選項可以一次性獲取所有檔案名稱。
- 使用 `-s` 選項時，確保擴展名正確，以避免意外刪除不必要的部分。
- 結合其他命令（如 `find` 或 `xargs`）使用 `basename` 可以提高效率，特別是在批量處理檔案時。