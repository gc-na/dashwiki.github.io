# [台灣] Debian Almquist Shell (dash) tee 用法: 將輸出寫入檔案

## Overview
`tee` 命令用於從標準輸入讀取資料，並同時將其寫入標準輸出和一個或多個檔案。這使得用戶能夠在查看輸出結果的同時，將資料保存到檔案中。

## Usage
基本語法如下：
```bash
tee [選項] [檔案...]
```

## Common Options
- `-a`：將輸出附加到指定的檔案，而不是覆蓋它。
- `-i`：忽略中斷信號。
- `-p`：在寫入檔案之前，將輸出顯示在標準輸出上。

## Common Examples
以下是一些常見的使用範例：

1. 將輸出寫入檔案：
   ```bash
   echo "Hello, World!" | tee output.txt
   ```

2. 將輸出附加到檔案：
   ```bash
   echo "Another line" | tee -a output.txt
   ```

3. 同時寫入多個檔案：
   ```bash
   echo "Logging data" | tee file1.txt file2.txt
   ```

4. 忽略中斷信號：
   ```bash
   cat /dev/urandom | tee -i random_data.txt
   ```

## Tips
- 使用 `-a` 選項可以避免覆蓋檔案，特別是在需要保留舊資料時。
- 結合 `|` 管道使用 `tee` 可以在處理長輸出時，方便地查看和保存資料。
- 確保檔案的寫入權限，以避免因權限問題導致的錯誤。