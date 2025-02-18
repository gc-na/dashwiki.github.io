# [中文] Debian Almquist Shell (dash) nohup 用法: 使进程在退出后继续运行

## 概述
`nohup` 命令用于在用户注销或关闭终端后，继续运行指定的命令。它可以防止进程接收到挂起信号，使得长时间运行的任务不会因为用户的退出而中断。

## 用法
基本语法如下：
```bash
nohup [选项] [命令] [参数] &
```

## 常用选项
- `-h`：显示帮助信息。
- `-p`：指定进程的优先级。
- `&`：将命令放入后台运行。

## 常见示例
1. 在后台运行一个脚本，并将输出重定向到 `nohup.out` 文件：
   ```bash
   nohup ./my_script.sh &
   ```

2. 运行一个长时间的下载命令，并将输出保存到指定文件：
   ```bash
   nohup wget http://example.com/largefile.zip -o download.log &
   ```

3. 启动一个 Python 服务器，并在后台运行：
   ```bash
   nohup python3 -m http.server 8000 &
   ```

## 提示
- 使用 `&` 将命令放入后台，这样可以继续使用终端。
- 定期检查 `nohup.out` 文件，以查看命令的输出和错误信息。
- 如果需要停止后台进程，可以使用 `kill` 命令结合进程 ID。