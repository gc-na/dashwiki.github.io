# [中文] Debian Almquist Shell (dash) gunzip 用法: 解压缩 gzip 文件

## 概述
`gunzip` 命令用于解压缩以 `.gz` 为扩展名的文件。它是 GNU zip 的一部分，常用于处理压缩文件，以节省存储空间。

## 用法
基本语法如下：
```
gunzip [选项] [参数]
```

## 常用选项
- `-c`：将解压缩的内容输出到标准输出，而不是替换原文件。
- `-f`：强制解压缩，即使目标文件已存在。
- `-k`：保留原始压缩文件。
- `-r`：递归解压缩目录中的所有 `.gz` 文件。

## 常见示例
1. 解压缩单个文件：
   ```bash
   gunzip example.txt.gz
   ```

2. 解压缩并保留原始文件：
   ```bash
   gunzip -k example.txt.gz
   ```

3. 将解压缩内容输出到标准输出：
   ```bash
   gunzip -c example.txt.gz > output.txt
   ```

4. 递归解压缩目录中的所有 `.gz` 文件：
   ```bash
   gunzip -r /path/to/directory
   ```

## 小贴士
- 在解压缩重要文件之前，建议先备份原始文件，以防数据丢失。
- 使用 `-c` 选项可以方便地查看压缩文件的内容，而无需实际解压缩文件。
- 结合使用 `tar` 和 `gunzip` 可以高效地处理归档和压缩文件，例如：`tar -xzvf archive.tar.gz`。