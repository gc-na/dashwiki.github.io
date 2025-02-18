# [中文] Debian Almquist Shell (dash) ftp 用法: 文件传输协议客户端

## 概述
`ftp` 命令是一个用于通过文件传输协议（FTP）与远程服务器进行交互的客户端工具。它允许用户上传、下载和管理服务器上的文件。

## 用法
基本语法如下：
```bash
ftp [options] [arguments]
```

## 常用选项
- `-i`：关闭交互式模式，适用于批量传输。
- `-n`：禁止自动登录，适合需要手动输入用户名和密码的情况。
- `-v`：启用详细模式，显示更多的传输信息。

## 常见示例
1. 连接到FTP服务器：
   ```bash
   ftp ftp.example.com
   ```

2. 使用用户名和密码连接：
   ```bash
   ftp -n ftp.example.com
   user your_username your_password
   ```

3. 下载文件：
   ```bash
   get remote_file.txt
   ```

4. 上传文件：
   ```bash
   put local_file.txt
   ```

5. 列出远程目录中的文件：
   ```bash
   ls
   ```

## 提示
- 在使用 `ftp` 进行文件传输时，确保使用安全的连接（如 SFTP）以保护敏感数据。
- 使用 `-i` 选项可以加快批量文件传输的速度。
- 定期检查和清理本地和远程目录，以避免不必要的文件堆积。