# [中文] Debian Almquist Shell (dash) traceroute 用法: 路由追踪工具

## 概述
`traceroute` 命令用于显示数据包在网络中从源主机到目标主机的路径。它通过发送带有逐步增加的 TTL（生存时间）值的数据包来确定经过的路由器，并测量每一跳的延迟。

## 用法
基本语法如下：
```bash
traceroute [options] [arguments]
```

## 常用选项
- `-m <hops>`: 设置最大跳数。
- `-n`: 以数字形式显示地址，而不是解析主机名。
- `-w <seconds>`: 设置等待每个响应的时间（默认是 5 秒）。
- `-p <port>`: 指定目标端口。

## 常见示例
1. 基本用法，追踪到目标主机：
   ```bash
   traceroute example.com
   ```

2. 使用数字格式显示地址：
   ```bash
   traceroute -n example.com
   ```

3. 设置最大跳数为 10：
   ```bash
   traceroute -m 10 example.com
   ```

4. 指定目标端口为 80：
   ```bash
   traceroute -p 80 example.com
   ```

5. 设置每个响应的等待时间为 2 秒：
   ```bash
   traceroute -w 2 example.com
   ```

## 提示
- 在使用 `traceroute` 时，确保你有足够的权限，因为某些网络可能会限制 ICMP 数据包。
- 使用 `-n` 选项可以加快输出速度，特别是在 DNS 解析较慢的情况下。
- 了解每一跳的延迟可以帮助你诊断网络问题，注意观察延迟较高的跳数。