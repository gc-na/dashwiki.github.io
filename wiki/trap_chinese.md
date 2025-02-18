# [中文] Debian Almquist Shell (dash) trap 用法: 捕获信号和执行清理操作

## 概述
`trap` 命令用于捕获信号并在接收到特定信号时执行指定的命令。这在脚本中非常有用，可以确保在脚本终止或中断时执行清理操作，例如删除临时文件或保存状态。

## 用法
基本语法如下：
```sh
trap [options] [commands] [signals]
```

## 常用选项
- `-p`：打印当前的 trap 设置。
- `-l`：列出所有可用的信号。
- `commands`：在接收到指定信号时执行的命令。
- `signals`：要捕获的信号列表，例如 `SIGINT`、`SIGTERM` 等。

## 常见示例
1. 捕获 `SIGINT` 信号并执行清理命令：
   ```sh
   trap 'echo "清理中..."; rm -f /tmp/tempfile' SIGINT
   ```

2. 在脚本退出时执行特定命令：
   ```sh
   trap 'echo "脚本已退出"; exit' EXIT
   ```

3. 捕获多个信号并执行相同的命令：
   ```sh
   trap 'echo "收到信号"; exit' SIGINT SIGTERM
   ```

4. 打印当前的 trap 设置：
   ```sh
   trap -p
   ```

## 提示
- 在使用 `trap` 时，确保在脚本的开始部分设置捕获信号，以便在整个脚本执行期间都能有效。
- 使用 `trap` 捕获 `EXIT` 信号，可以确保在脚本结束时执行清理操作，无论是正常退出还是由于错误退出。
- 记得在捕获信号后，使用 `exit` 命令来终止脚本，以避免继续执行后续命令。