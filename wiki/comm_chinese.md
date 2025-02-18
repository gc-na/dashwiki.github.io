# [中文] Debian Almquist Shell (dash) comm 命令: 比较文件行

## 概述
`comm` 命令用于比较两个已排序文件的内容，并输出它们的差异。它可以显示两个文件中独有的行、两个文件共有的行，以及它们的组合。

## 用法
基本语法如下：
```
comm [选项] [文件1] [文件2]
```

## 常用选项
- `-1`：不显示文件1中独有的行。
- `-2`：不显示文件2中独有的行。
- `-3`：不显示两个文件中共有的行。
- `-i`：在比较时忽略大小写。

## 常见示例
1. 比较两个文件并输出所有差异：
   ```bash
   comm file1.txt file2.txt
   ```

2. 仅显示文件1中独有的行：
   ```bash
   comm -13 file1.txt file2.txt
   ```

3. 仅显示文件2中独有的行：
   ```bash
   comm -12 file1.txt file2.txt
   ```

4. 忽略大小写进行比较：
   ```bash
   comm -i file1.txt file2.txt
   ```

## 提示
- 确保输入的文件是已排序的，否则结果可能不正确。
- 使用 `sort` 命令对文件进行排序，例如：
  ```bash
  sort file1.txt -o file1.txt
  sort file2.txt -o file2.txt
  ```
- 可以将 `comm` 命令与其他命令结合使用，以实现更复杂的文本处理任务。