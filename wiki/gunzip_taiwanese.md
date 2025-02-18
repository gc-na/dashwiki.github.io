# [台灣] Debian Almquist Shell (dash) gunzip 使用方式: 解壓縮 gzip 檔案

## Overview
`gunzip` 是一個用於解壓縮 `.gz` 檔案的命令。它能夠將經過 gzip 壓縮的檔案恢復到原始狀態，方便使用者訪問和處理這些檔案。

## Usage
基本語法如下：
```
gunzip [options] [arguments]
```

## Common Options
- `-c`：將解壓縮的內容輸出到標準輸出，不會改變原始檔案。
- `-f`：強制解壓縮，即使檔案已經存在或有錯誤。
- `-k`：保留原始的 `.gz` 檔案，解壓縮後仍然保留壓縮檔。
- `-v`：顯示詳細的解壓縮過程。

## Common Examples
以下是一些常見的使用範例：

1. 解壓縮單個檔案：
   ```bash
   gunzip file.txt.gz
   ```

2. 解壓縮並保留原始檔案：
   ```bash
   gunzip -k file.txt.gz
   ```

3. 將解壓縮內容輸出到標準輸出：
   ```bash
   gunzip -c file.txt.gz > output.txt
   ```

4. 強制解壓縮檔案：
   ```bash
   gunzip -f file.txt.gz
   ```

5. 顯示解壓縮過程：
   ```bash
   gunzip -v file.txt.gz
   ```

## Tips
- 在解壓縮之前，確認檔案的完整性，以避免損壞的檔案導致解壓縮失敗。
- 使用 `-k` 選項可以保留原始檔案，這對於需要保留壓縮檔以備未來使用的情況特別有用。
- 如果需要解壓縮多個檔案，可以將它們一起列出：
  ```bash
  gunzip file1.gz file2.gz file3.gz
  ```