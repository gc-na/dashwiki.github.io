# [中文] Debian Almquist Shell (dash) killall 使用方法: 终止进程

## 概述
`killall` 命令用于终止指定名称的所有进程。它可以通过进程名称来查找并杀死进程，而不需要知道进程的 PID（进程标识符）。

## 用法
基本语法如下：
```bash
killall [选项] [进程名称]
```

## 常用选项
- `-u`：仅终止指定用户拥有的进程。
- `-q`：安静模式，不显示错误信息。
- `-I`：忽略大小写，匹配进程名称时不区分大小写。
- `-s`：指定发送的信号，默认为 `TERM` 信号。

## 常见示例
1. 终止所有名为 `firefox` 的进程：
   ```bash
   killall firefox
   ```

2. 终止所有名为 `ssh` 的进程，并且只终止当前用户的进程：
   ```bash
   killall -u $(whoami) ssh
   ```

3. 使用安静模式终止所有名为 `myapp` 的进程：
   ```bash
   killall -q myapp
   ```

4. 发送 `SIGKILL` 信号终止所有名为 `sleep` 的进程：
   ```bash
   killall -s KILL sleep
   ```

## 提示
- 在使用 `killall` 时，请确保您有权限终止指定的进程。
- 使用 `-q` 选项可以避免在进程不存在时显示错误信息。
- 在终止进程之前，您可以使用 `pgrep` 命令来确认要终止的进程是否存在。