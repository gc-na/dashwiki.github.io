# [中文] Debian Almquist Shell (dash) basename 用法等价: 提取文件名

## 概述
`basename` 命令用于从给定的路径中提取文件名部分，去掉路径和可选的文件扩展名。这在处理文件路径时非常有用，尤其是在脚本中需要仅获取文件名的场景。

## 用法
基本语法如下：
```
basename [options] [arguments]
```

## 常用选项
- `-a`：处理多个路径，返回每个路径的文件名。
- `-s`：去掉指定的后缀名。
- `--help`：显示帮助信息。

## 常见示例
1. 提取文件名：
   ```sh
   basename /usr/local/bin/script.sh
   ```
   输出：
   ```
   script.sh
   ```

2. 去掉文件扩展名：
   ```sh
   basename /usr/local/bin/script.sh .sh
   ```
   输出：
   ```
   script
   ```

3. 处理多个路径：
   ```sh
   basename -a /usr/local/bin/script.sh /home/user/docs/report.txt
   ```
   输出：
   ```
   script.sh
   report.txt
   ```

4. 去掉自定义后缀：
   ```sh
   basename /home/user/file.txt .txt
   ```
   输出：
   ```
   file
   ```

## 提示
- 在使用 `basename` 时，确保路径格式正确，以避免意外的输出。
- 可以结合其他命令使用 `basename`，例如在脚本中处理文件列表时。
- 使用 `-a` 选项可以一次性处理多个文件路径，节省时间。