# [台灣] Debian Almquist Shell (dash) uniq 使用方法: 刪除重複的行

## Overview
`uniq` 命令用於從已排序的檔案中刪除重複的行。它會比較相鄰的行，並只保留唯一的行，這使得它在處理文本數據時非常有用。

## Usage
基本語法如下：
```
uniq [選項] [參數]
```

## Common Options
- `-c`：計算每行出現的次數，並在行前顯示計數。
- `-d`：只顯示重複的行。
- `-u`：只顯示唯一的行。
- `-i`：忽略大小寫的差異。

## Common Examples
1. 刪除重複行並顯示唯一行：
   ```bash
   sort input.txt | uniq
   ```

2. 計算每行出現的次數：
   ```bash
   sort input.txt | uniq -c
   ```

3. 顯示重複的行：
   ```bash
   sort input.txt | uniq -d
   ```

4. 顯示唯一的行：
   ```bash
   sort input.txt | uniq -u
   ```

5. 忽略大小寫的重複行：
   ```bash
   sort input.txt | uniq -i
   ```

## Tips
- 確保在使用 `uniq` 之前先對檔案進行排序，因為 `uniq` 只比較相鄰的行。
- 可以將 `uniq` 與其他命令結合使用，例如 `sort`，以處理更複雜的文本處理任務。
- 使用 `-c` 選項時，可以快速了解哪些行是最常出現的，這對於數據分析特別有用。