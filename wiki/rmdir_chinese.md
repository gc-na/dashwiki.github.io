# [中文] Debian Almquist Shell (dash) rmdir 使用方法: 删除空目录

## Overview
`rmdir` 命令用于删除空目录。如果目录中包含文件或其他目录，`rmdir` 将无法删除该目录。

## Usage
基本语法如下：
```
rmdir [选项] [参数]
```

## Common Options
- `--help`：显示帮助信息。
- `--verbose`：在删除目录时显示详细信息。

## Common Examples
以下是一些常用的 `rmdir` 示例：

1. 删除一个空目录：
   ```bash
   rmdir my_empty_directory
   ```

2. 删除多个空目录：
   ```bash
   rmdir dir1 dir2 dir3
   ```

3. 显示详细信息：
   ```bash
   rmdir --verbose my_empty_directory
   ```

4. 显示帮助信息：
   ```bash
   rmdir --help
   ```

## Tips
- 在使用 `rmdir` 之前，确保目录是空的，可以使用 `ls` 命令检查目录内容。
- 如果需要删除非空目录，请使用 `rm -r` 命令，但要小心，因为这将删除目录及其所有内容。