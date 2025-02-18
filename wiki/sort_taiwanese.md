# [台灣] Debian Almquist Shell (dash) sort 用法: 排序文本行

## Overview
`sort` 命令用於將文本行進行排序，根據字母順序或數字順序排列，並可以處理多種選項來自定義排序方式。

## Usage
基本語法如下：
```
sort [options] [arguments]
```

## Common Options
- `-r`: 反向排序，從高到低。
- `-n`: 按數字排序，而不是字母排序。
- `-k`: 指定排序的鍵，允許根據特定欄位排序。
- `-u`: 刪除重複的行，只保留唯一的行。

## Common Examples
- 按字母順序排序文件內容：
  ```sh
  sort filename.txt
  ```

- 反向排序文件內容：
  ```sh
  sort -r filename.txt
  ```

- 按數字排序：
  ```sh
  sort -n numbers.txt
  ```

- 根據第二欄進行排序：
  ```sh
  sort -k 2 filename.txt
  ```

- 刪除重複行並排序：
  ```sh
  sort -u filename.txt
  ```

## Tips
- 使用 `-o` 選項可以將排序結果直接輸出到文件中，例如：
  ```sh
  sort filename.txt -o sorted.txt
  ```
- 結合 `-k` 和 `-n` 可以更精確地控制排序行為，特別是當處理包含數字的文本時。
- 在處理大型文件時，考慮使用 `-S` 選項來指定可用的內存，以提高性能。