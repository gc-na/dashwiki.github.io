# [中文] Debian Almquist Shell (dash) wget 用法: 下载文件的命令

## 概述
`wget` 是一个用于从网络上下载文件的命令行工具。它支持 HTTP、HTTPS 和 FTP 协议，能够在不需要用户交互的情况下下载文件。

## 用法
基本语法如下：
```bash
wget [选项] [参数]
```

## 常用选项
- `-O <文件名>`: 指定下载文件的保存名称。
- `-q`: 安静模式，不显示下载进度。
- `-c`: 断点续传，继续未完成的下载。
- `--limit-rate=<速率>`: 限制下载速度。
- `-r`: 递归下载，用于下载整个网站。

## 常见示例
1. 下载单个文件：
   ```bash
   wget http://example.com/file.zip
   ```

2. 指定保存文件名：
   ```bash
   wget -O myfile.zip http://example.com/file.zip
   ```

3. 断点续传：
   ```bash
   wget -c http://example.com/largefile.zip
   ```

4. 限制下载速度：
   ```bash
   wget --limit-rate=200k http://example.com/file.zip
   ```

5. 递归下载整个网站：
   ```bash
   wget -r http://example.com/
   ```

## 提示
- 使用 `-q` 选项可以在后台下载文件，避免干扰终端操作。
- 对于大文件下载，建议使用 `-c` 选项，以防网络中断。
- 在下载多个文件时，可以将 URL 列表放在一个文本文件中，然后使用 `-i` 选项批量下载：
  ```bash
  wget -i urls.txt
  ```