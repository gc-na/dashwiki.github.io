# [中文] Debian Almquist Shell (dash) diff 用法: 比较文件差异

## 概述
`diff` 命令用于比较两个文件的内容，并显示它们之间的差异。它通常用于查看文本文件的变化，特别是在版本控制和代码审查中非常有用。

## 用法
基本语法如下：
```bash
diff [选项] [文件1] [文件2]
```

## 常用选项
- `-u`：以统一格式显示差异，便于阅读。
- `-c`：以上下文格式显示差异，提供更多的上下文信息。
- `-i`：忽略大小写的差异。
- `-w`：忽略所有空格的差异。

## 常见示例
1. 比较两个文本文件的差异：
   ```bash
   diff file1.txt file2.txt
   ```

2. 使用统一格式显示差异：
   ```bash
   diff -u file1.txt file2.txt
   ```

3. 忽略大小写进行比较：
   ```bash
   diff -i file1.txt file2.txt
   ```

4. 显示上下文格式的差异：
   ```bash
   diff -c file1.txt file2.txt
   ```

5. 忽略空格进行比较：
   ```bash
   diff -w file1.txt file2.txt
   ```

## 提示
- 在使用 `diff` 时，建议先使用 `-u` 选项，这样可以更清晰地看到差异。
- 如果需要将差异输出到文件，可以使用重定向：
  ```bash
  diff file1.txt file2.txt > differences.txt
  ```
- 在版本控制中，结合 `diff` 和 `patch` 命令，可以方便地应用和管理文件的更改。