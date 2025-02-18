# [台灣] Debian Almquist Shell (dash) bunzip2 使用方法: 解壓縮 bzip2 格式的檔案

## Overview
`bunzip2` 是一個用於解壓縮 bzip2 格式檔案的命令。它可以將壓縮的檔案還原為原始檔案，方便用戶使用。

## Usage
基本語法如下：
```
bunzip2 [選項] [檔案]
```

## Common Options
- `-k`：保留原始的壓縮檔案。
- `-f`：強制解壓縮，即使檔案已存在。
- `-v`：顯示詳細的解壓縮過程。

## Common Examples
以下是一些常見的使用範例：

1. 解壓縮單個檔案：
   ```bash
   bunzip2 example.bz2
   ```

2. 解壓縮並保留原始檔案：
   ```bash
   bunzip2 -k example.bz2
   ```

3. 強制解壓縮已存在的檔案：
   ```bash
   bunzip2 -f example.bz2
   ```

4. 顯示解壓縮過程：
   ```bash
   bunzip2 -v example.bz2
   ```

## Tips
- 使用 `-k` 選項可以避免意外刪除原始檔案，特別是在不確定的情況下。
- 在批量解壓縮檔案時，可以使用通配符，例如：
  ```bash
  bunzip2 *.bz2
  ```
- 確保在解壓縮之前檔案的完整性，以避免損壞的檔案導致解壓失敗。