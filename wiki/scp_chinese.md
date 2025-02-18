# [中文] Debian Almquist Shell (dash) scp 用法: 复制文件和目录

## 概述
`scp`（安全复制）命令用于在本地主机和远程主机之间安全地复制文件和目录。它基于SSH协议，确保数据在传输过程中的安全性。

## 用法
基本语法如下：
```bash
scp [选项] [源] [目标]
```

## 常用选项
- `-r`：递归复制整个目录。
- `-P`：指定远程主机的端口号（注意是大写的P）。
- `-i`：指定用于身份验证的私钥文件。
- `-v`：显示详细的操作过程，用于调试。

## 常见示例
1. 从本地复制文件到远程主机：
   ```bash
   scp /path/to/local/file username@remote_host:/path/to/remote/directory
   ```

2. 从远程主机复制文件到本地：
   ```bash
   scp username@remote_host:/path/to/remote/file /path/to/local/directory
   ```

3. 递归复制整个目录到远程主机：
   ```bash
   scp -r /path/to/local/directory username@remote_host:/path/to/remote/directory
   ```

4. 使用指定的端口号进行复制：
   ```bash
   scp -P 2222 /path/to/local/file username@remote_host:/path/to/remote/directory
   ```

## 提示
- 确保SSH服务在远程主机上运行，以便使用`scp`命令。
- 使用`-v`选项可以帮助你诊断连接问题。
- 在处理大文件时，可以考虑使用`-C`选项启用压缩，以加快传输速度。