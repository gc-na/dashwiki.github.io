# [中文] Debian Almquist Shell (dash) dig 用法: 查询DNS信息

## 概述
`dig` 命令用于查询DNS（域名系统）信息。它可以帮助用户获取域名的解析记录，包括A记录、MX记录、CNAME记录等，常用于网络故障排除和DNS配置验证。

## 用法
基本语法如下：
```
dig [选项] [参数]
```

## 常用选项
- `@server`：指定要查询的DNS服务器。
- `-t type`：指定查询的记录类型，如A、MX、CNAME等。
- `+short`：以简短格式输出结果。
- `+trace`：追踪DNS解析过程。

## 常见示例
1. 查询某个域名的A记录：
   ```bash
   dig example.com
   ```

2. 查询特定DNS服务器的A记录：
   ```bash
   dig @8.8.8.8 example.com
   ```

3. 查询MX记录：
   ```bash
   dig -t MX example.com
   ```

4. 使用简短格式输出结果：
   ```bash
   dig +short example.com
   ```

5. 追踪DNS解析过程：
   ```bash
   dig +trace example.com
   ```

## 提示
- 使用 `+short` 选项可以快速获取简洁的结果，适合快速查看。
- 在进行DNS故障排除时，可以尝试不同的DNS服务器，以确认问题是否出在特定的服务器上。
- 了解不同的记录类型有助于更有效地使用 `dig` 命令。