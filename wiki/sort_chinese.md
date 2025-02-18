# [中文] Debian Almquist Shell (dash) sort 用法: 排序文本行

## 概述
`sort` 命令用于对文本文件中的行进行排序。它可以根据字母顺序、数字顺序或其他自定义规则对输入进行排序，并将结果输出到标准输出或文件中。

## 用法
基本语法如下：
```bash
sort [options] [arguments]
```

## 常用选项
- `-n`：按数字顺序排序。
- `-r`：以逆序排列。
- `-k`：指定排序的关键字列。
- `-u`：只输出唯一的行。
- `-o`：将输出结果写入指定文件。

## 常见示例
1. 按字母顺序排序文件内容：
   ```bash
   sort filename.txt
   ```

2. 按数字顺序排序：
   ```bash
   sort -n numbers.txt
   ```

3. 逆序排列文件内容：
   ```bash
   sort -r filename.txt
   ```

4. 按指定列排序（例如，第二列）：
   ```bash
   sort -k 2 filename.txt
   ```

5. 输出唯一行到新文件：
   ```bash
   sort -u filename.txt -o unique.txt
   ```

## 提示
- 在处理大文件时，可以使用 `-o` 选项直接将结果写入文件，以节省内存。
- 使用 `-k` 选项时，确保指定的列存在于输入文件中。
- 结合其他命令（如 `grep` 或 `awk`）使用 `sort` 可以实现更复杂的数据处理。