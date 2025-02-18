# [中文] Debian Almquist Shell (dash) sed 用法: 文本流编辑器

## 概述
`sed` 是一个强大的文本流编辑器，用于对输入文本进行处理和转换。它可以执行查找、替换、插入和删除等操作，通常用于处理文件或标准输入中的文本数据。

## 用法
基本语法如下：
```bash
sed [options] [arguments]
```

## 常用选项
- `-e`：允许在命令行中指定多个编辑命令。
- `-f`：从文件中读取编辑命令。
- `-i`：直接在文件中进行修改，而不是输出到标准输出。
- `-n`：抑制默认输出，仅输出通过 `p` 命令指定的行。

## 常见示例
1. **替换文本**
   将文件中的 "apple" 替换为 "orange"：
   ```bash
   sed 's/apple/orange/g' filename.txt
   ```

2. **删除行**
   删除文件中的第2行：
   ```bash
   sed '2d' filename.txt
   ```

3. **插入行**
   在第3行之前插入 "New Line"：
   ```bash
   sed '3i New Line' filename.txt
   ```

4. **从文件中读取命令**
   使用命令文件 `commands.sed`：
   ```bash
   sed -f commands.sed filename.txt
   ```

5. **直接修改文件**
   直接在文件中替换 "cat" 为 "dog"：
   ```bash
   sed -i 's/cat/dog/g' filename.txt
   ```

## 提示
- 在使用 `-i` 选项时，可以考虑备份原文件，例如 `-i.bak`，这样会生成一个 `.bak` 的备份文件。
- 使用 `-n` 选项时，结合 `p` 命令可以更精确地控制输出。
- 在复杂的替换中，使用分隔符（如 `|`）可以避免与文本中的 `/` 冲突。