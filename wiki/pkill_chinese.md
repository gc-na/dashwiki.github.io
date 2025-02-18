# [中文] Debian Almquist Shell (dash) pkill 用法: 终止进程

## 概述
`pkill` 命令用于根据进程名称或其他属性终止正在运行的进程。它提供了一种方便的方式来管理系统中的进程，而无需查找进程 ID（PID）。

## 用法
基本语法如下：
```
pkill [选项] [参数]
```

## 常用选项
- `-f`：匹配完整的命令行，而不仅仅是进程名称。
- `-n`：终止最新启动的进程。
- `-o`：终止最早启动的进程。
- `-signal`：指定要发送的信号，默认是 `TERM` 信号。

## 常见示例
1. 终止名为 `myprocess` 的所有进程：
   ```bash
   pkill myprocess
   ```

2. 终止所有包含 `python` 的进程：
   ```bash
   pkill -f python
   ```

3. 终止最新启动的 `httpd` 进程：
   ```bash
   pkill -n httpd
   ```

4. 发送 `SIGKILL` 信号终止名为 `myapp` 的进程：
   ```bash
   pkill -9 myapp
   ```

## 提示
- 使用 `pkill` 时要小心，以免意外终止重要的系统进程。
- 可以使用 `pgrep` 命令先查看匹配的进程，确保你要终止的进程是正确的。
- 在脚本中使用 `pkill` 时，考虑添加日志记录，以便追踪终止的进程。