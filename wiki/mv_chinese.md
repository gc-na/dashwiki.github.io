# [中文] Debian Almquist Shell (dash) mv 用法: 移动或重命名文件和目录

## 概述
`mv` 命令用于移动或重命名文件和目录。它可以将一个文件从一个位置移动到另一个位置，或者改变文件的名称。

## 用法
基本语法如下：
```bash
mv [选项] [源] [目标]
```

## 常用选项
- `-i`：在覆盖文件之前提示确认。
- `-u`：仅在源文件比目标文件新或目标文件不存在时才移动文件。
- `-v`：在移动文件时显示详细信息。

## 常见示例
1. **移动文件到另一个目录**
   ```bash
   mv file.txt /path/to/directory/
   ```

2. **重命名文件**
   ```bash
   mv oldname.txt newname.txt
   ```

3. **移动并重命名文件**
   ```bash
   mv file.txt /path/to/directory/newfile.txt
   ```

4. **使用交互模式防止覆盖**
   ```bash
   mv -i file.txt /path/to/directory/
   ```

5. **仅在源文件更新时移动**
   ```bash
   mv -u file.txt /path/to/directory/
   ```

## 提示
- 在使用 `mv` 命令时，确保目标路径是正确的，以避免意外覆盖文件。
- 使用 `-i` 选项可以有效防止数据丢失，特别是在处理重要文件时。
- 如果需要移动多个文件，可以将它们列在源参数中，例如：
  ```bash
  mv file1.txt file2.txt /path/to/directory/
  ```