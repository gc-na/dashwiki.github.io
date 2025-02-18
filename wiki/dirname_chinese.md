# [中文] Debian Almquist Shell (dash) dirname 用法: 提取文件路径中的目录部分

## 概述
`dirname` 命令用于从给定的文件路径中提取目录部分。它返回去掉文件名后的路径，常用于脚本和命令行操作中，以便获取文件所在的目录。

## 用法
基本语法如下：
```bash
dirname [options] [arguments]
```

## 常用选项
- `-z`：以空字符作为分隔符，而不是换行符，适用于处理包含换行符的路径。
- `--help`：显示帮助信息。
- `--version`：显示版本信息。

## 常见示例
1. 提取单个文件路径的目录部分：
   ```bash
   dirname /usr/local/bin/script.sh
   ```
   输出：
   ```
   /usr/local/bin
   ```

2. 提取多个文件路径的目录部分：
   ```bash
   dirname /etc/nginx/nginx.conf /var/log/syslog
   ```
   输出：
   ```
   /etc/nginx
   /var/log
   ```

3. 使用空字符作为分隔符：
   ```bash
   dirname -z "/usr/local/bin/script.sh\0/usr/bin/another_script.sh"
   ```
   输出：
   ```
   /usr/local/bin
   /usr/bin
   ```

## 小贴士
- 在处理多个路径时，可以将它们作为参数传递给 `dirname`，以便一次性提取所有目录。
- 在脚本中使用 `dirname` 时，可以结合其他命令（如 `cd`）来改变当前工作目录。
- 注意路径的格式，确保使用绝对路径或相对路径，以避免意外的结果。