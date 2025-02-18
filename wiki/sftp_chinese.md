# [中文] Debian Almquist Shell (dash) sftp 用法: 传输文件的安全协议

## 概述
`sftp`（安全文件传输协议）是一个用于在网络上安全地传输文件的命令行工具。它通过SSH（安全外壳协议）提供加密的文件传输，确保数据的安全性和完整性。

## 用法
基本语法如下：
```bash
sftp [options] [user@]host
```

## 常用选项
- `-b batchfile`：使用批处理文件中的命令。
- `-C`：启用压缩以加快传输速度。
- `-i identity_file`：指定用于身份验证的私钥文件。
- `-P port`：指定连接的端口号。
- `-v`：启用详细模式，显示调试信息。

## 常见示例
1. 连接到远程主机：
   ```bash
   sftp user@hostname
   ```

2. 从远程主机下载文件：
   ```bash
   sftp user@hostname:/path/to/remote/file /path/to/local/directory
   ```

3. 上传文件到远程主机：
   ```bash
   sftp /path/to/local/file user@hostname:/path/to/remote/directory
   ```

4. 使用批处理文件执行多个命令：
   ```bash
   sftp -b batchfile.txt user@hostname
   ```

5. 启用压缩传输文件：
   ```bash
   sftp -C user@hostname
   ```

## 提示
- 在使用`sftp`时，确保SSH服务在远程主机上运行。
- 使用公钥认证可以提高安全性，避免输入密码。
- 定期检查和更新SSH密钥，以确保安全性。
- 在传输大文件时，考虑使用压缩选项以提高效率。