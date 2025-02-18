# [中文] Debian Almquist Shell (dash) tee 用法: 将输入复制到输出文件

## 概述
`tee` 命令用于从标准输入读取数据，并将其同时输出到标准输出和一个或多个文件中。这在需要查看输出的同时保存输出内容时非常有用。

## 用法
基本语法如下：
```bash
tee [选项] [文件...]
```

## 常用选项
- `-a`：以附加模式打开文件，而不是覆盖模式。
- `-i`：忽略中断信号。
- `--help`：显示帮助信息。

## 常见示例
1. 将输出保存到文件并显示在终端：
   ```bash
   echo "Hello, World!" | tee output.txt
   ```

2. 将输出附加到现有文件中：
   ```bash
   echo "Another line" | tee -a output.txt
   ```

3. 将多个文件的输出同时写入不同的文件：
   ```bash
   echo "Line 1" | tee file1.txt file2.txt
   ```

4. 从命令的输出中获取并保存：
   ```bash
   ls -l | tee directory_listing.txt
   ```

## 小贴士
- 使用 `-a` 选项可以避免覆盖文件内容，特别是在需要保留历史记录时。
- 结合管道使用 `tee` 可以在调试脚本时查看中间输出。
- 确保有适当的文件权限，以便 `tee` 可以写入指定的文件。