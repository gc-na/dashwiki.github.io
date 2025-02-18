# [中文] Debian Almquist Shell (dash) export 用法等价: 设置环境变量

## 概述
`export` 命令用于设置或导出环境变量，使得在当前 shell 会话中以及其子进程中可用。通过使用 `export`，用户可以将变量的值传递给其他程序和脚本。

## 用法
基本语法如下：
```bash
export [options] [arguments]
```

## 常用选项
- `-p`：显示所有导出的环境变量。
- `-n`：取消导出指定的变量，使其不再是环境变量。
- `-f`：导出函数，而不仅仅是变量。

## 常见示例
1. 导出一个变量：
   ```bash
   MY_VAR="Hello, World!"
   export MY_VAR
   ```

2. 直接导出并赋值：
   ```bash
   export MY_VAR="Hello, World!"
   ```

3. 查看所有导出的环境变量：
   ```bash
   export -p
   ```

4. 取消导出一个变量：
   ```bash
   export -n MY_VAR
   ```

5. 导出一个函数：
   ```bash
   my_function() {
       echo "This is a function."
   }
   export -f my_function
   ```

## 小贴士
- 在脚本中使用 `export` 可以确保变量在子进程中可用。
- 使用 `export -p` 可以快速检查当前会话中的所有环境变量。
- 记得在使用 `export` 之前，先确认变量是否已经定义，以避免不必要的错误。