# [中文] Debian Almquist Shell (dash) bunzip2 用法: 解压缩 bzip2 格式文件

## 概述
`bunzip2` 命令用于解压缩使用 bzip2 压缩算法压缩的文件。它通常用于处理以 `.bz2` 后缀结尾的文件，能够有效地减小文件大小。

## 用法
基本语法如下：
```bash
bunzip2 [选项] [参数]
```

## 常用选项
- `-k`：保留原始的压缩文件。
- `-f`：强制解压缩，即使目标文件已存在。
- `-v`：显示详细的解压缩过程。

## 常见示例
- 解压缩一个文件：
```bash
bunzip2 example.bz2
```

- 解压缩并保留原始文件：
```bash
bunzip2 -k example.bz2
```

- 强制解压缩文件：
```bash
bunzip2 -f example.bz2
```

- 显示解压缩过程的详细信息：
```bash
bunzip2 -v example.bz2
```

## 提示
- 在解压缩大文件时，确保有足够的磁盘空间。
- 使用 `-k` 选项可以避免数据丢失，特别是在处理重要文件时。
- 如果你需要解压缩多个文件，可以使用通配符，例如：
```bash
bunzip2 *.bz2
```