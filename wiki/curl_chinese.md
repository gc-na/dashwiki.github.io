# [中文] Debian Almquist Shell (dash) curl 使用方法: 进行数据传输的命令行工具

## 概述
`curl` 是一个用于在命令行中进行数据传输的工具，支持多种协议，包括 HTTP、HTTPS、FTP 等。它可以用来下载文件、发送数据以及与网络服务进行交互。

## 用法
基本语法如下：
```bash
curl [选项] [参数]
```

## 常用选项
- `-O`：将下载的文件保存为远程文件的名称。
- `-o <file>`：将下载的内容保存到指定的文件中。
- `-I`：仅获取 HTTP 响应头。
- `-d <data>`：发送 POST 请求时附加的数据。
- `-H <header>`：添加自定义 HTTP 头部。

## 常见示例
1. 下载文件并保存为原始文件名：
   ```bash
   curl -O http://example.com/file.zip
   ```

2. 下载文件并保存为指定名称：
   ```bash
   curl -o myfile.zip http://example.com/file.zip
   ```

3. 获取网页的 HTTP 响应头：
   ```bash
   curl -I http://example.com
   ```

4. 发送 POST 请求并附加数据：
   ```bash
   curl -d "name=John&age=30" http://example.com/api
   ```

5. 添加自定义 HTTP 头部：
   ```bash
   curl -H "Authorization: Bearer token" http://example.com/api
   ```

## 小贴士
- 使用 `-v` 选项可以查看详细的请求和响应信息，便于调试。
- 对于需要身份验证的请求，可以使用 `-u <username>:<password>` 来提供凭据。
- 如果需要下载大文件，可以使用 `-C -` 选项来支持断点续传。