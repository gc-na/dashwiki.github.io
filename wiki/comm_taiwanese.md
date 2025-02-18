# [台灣] Debian Almquist Shell (dash) comm 命令: 比較文件的行

## Overview
`comm` 命令用於比較兩個已排序的文件，並顯示它們之間的差異。這個命令會將兩個文件的內容進行比對，並將結果分為三個部分：僅在第一個文件中的行、僅在第二個文件中的行，以及兩個文件中都存在的行。

## Usage
基本語法如下：
```
comm [選項] [文件1] [文件2]
```

## Common Options
- `-1`：不顯示僅在第一個文件中的行。
- `-2`：不顯示僅在第二個文件中的行。
- `-3`：不顯示在兩個文件中都存在的行。
- `-i`：在比較時忽略大小寫。

## Common Examples
以下是一些常見的使用範例：

1. 比較兩個文件並顯示所有差異：
   ```bash
   comm file1.txt file2.txt
   ```

2. 僅顯示僅在第一個文件中的行：
   ```bash
   comm -13 file1.txt file2.txt
   ```

3. 僅顯示僅在第二個文件中的行：
   ```bash
   comm -12 file1.txt file2.txt
   ```

4. 忽略大小寫進行比較：
   ```bash
   comm -i file1.txt file2.txt
   ```

## Tips
- 確保在使用 `comm` 命令之前，對比的文件已經排序，否則結果可能不正確。
- 可以使用 `sort` 命令來排序文件，例如：
  ```bash
  sort file1.txt -o file1.txt
  sort file2.txt -o file2.txt
  ```
- 使用 `comm` 命令時，考慮將輸出重定向到文件，以便後續查看：
  ```bash
  comm file1.txt file2.txt > output.txt
  ```