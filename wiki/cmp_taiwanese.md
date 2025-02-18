# [台灣] Debian Almquist Shell (dash) cmp 使用法: 比較兩個檔案的內容

## Overview
`cmp` 命令用來比較兩個檔案的內容，並且在發現不同之處時，會顯示出來。這個命令通常用於檢查檔案是否相同，特別是在處理二進位檔案時。

## Usage
基本語法如下：
```
cmp [options] [arguments]
```

## Common Options
- `-l`: 列出所有不同的位元組及其位置。
- `-s`: 靜默模式，只返回退出狀態，不顯示任何輸出。
- `-i OFFSET`: 從指定的位移開始比較檔案。
- `-n N`: 只比較前 N 個位元組。

## Common Examples
1. 比較兩個檔案：
   ```bash
   cmp file1.txt file2.txt
   ```

2. 使用靜默模式，只返回狀態碼：
   ```bash
   cmp -s file1.txt file2.txt
   ```

3. 列出所有不同的位元組及其位置：
   ```bash
   cmp -l file1.bin file2.bin
   ```

4. 從指定的位移開始比較：
   ```bash
   cmp -i 10 file1.txt file2.txt
   ```

5. 只比較前 20 個位元組：
   ```bash
   cmp -n 20 file1.txt file2.txt
   ```

## Tips
- 在比較大檔案時，使用 `-s` 選項可以快速檢查檔案是否相同，而不需要顯示詳細的差異。
- 當處理二進位檔案時，使用 `-l` 選項可以幫助你找出具體的差異位置。
- 如果只想比較檔案的前幾個位元組，使用 `-n` 選項可以提高效率。