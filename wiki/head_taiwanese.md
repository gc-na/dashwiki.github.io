# [台灣] Debian Almquist Shell (dash) head 用法: 顯示檔案的前幾行

## Overview
`head` 命令用來顯示檔案的前幾行，通常用於快速查看檔案的開頭部分。這對於檢查檔案內容或確認檔案格式非常有用。

## Usage
基本語法如下：
```
head [options] [arguments]
```

## Common Options
- `-n NUM`：顯示檔案的前 NUM 行，預設為 10 行。
- `-c NUM`：顯示檔案的前 NUM 字元。
- `-q`：在多個檔案時不顯示檔案名稱。
- `-v`：在多個檔案時顯示檔案名稱。

## Common Examples
以下是一些常見的使用範例：

1. 顯示檔案的前 10 行（預設行數）：
   ```bash
   head filename.txt
   ```

2. 顯示檔案的前 5 行：
   ```bash
   head -n 5 filename.txt
   ```

3. 顯示檔案的前 20 字元：
   ```bash
   head -c 20 filename.txt
   ```

4. 顯示多個檔案的前 10 行，並顯示檔案名稱：
   ```bash
   head -v file1.txt file2.txt
   ```

5. 顯示多個檔案的前 5 行，但不顯示檔案名稱：
   ```bash
   head -q -n 5 file1.txt file2.txt
   ```

## Tips
- 使用 `head` 可以快速檢查檔案格式，特別是當檔案很大時。
- 結合其他命令，如 `grep`，可以更有效地篩選出需要的資料。
- 在處理大型日誌檔案時，`head` 是一個非常有用的工具，可以快速查看最新的記錄。