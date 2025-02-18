# [中文] Debian Almquist Shell (dash) logout 用法等价: 退出当前会话

## 概述
`logout` 命令用于退出当前的 shell 会话。它通常在登录的 shell 中使用，当用户希望结束会话并返回到登录提示时，可以使用此命令。

## 用法
基本语法如下：
```
logout [options]
```

## 常用选项
- `-n`：不显示任何消息。
- `-f`：强制退出，不提示确认。

## 常见示例
以下是一些常见的使用示例：

1. 退出当前 shell 会话：
   ```sh
   logout
   ```

2. 强制退出当前 shell 会话：
   ```sh
   logout -f
   ```

3. 退出时不显示任何消息：
   ```sh
   logout -n
   ```

## 提示
- 在使用 `logout` 命令之前，请确保已保存所有未保存的工作，以免丢失数据。
- 如果您在嵌套的 shell 中使用 `logout`，请注意它只会退出最内层的 shell。
- 对于非登录 shell，使用 `exit` 命令可能更为合适。