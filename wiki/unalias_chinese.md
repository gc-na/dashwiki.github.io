# [中文] Debian Almquist Shell (dash) unalias 用法: 删除别名

## 概述
`unalias` 命令用于删除在当前 shell 会话中定义的别名。别名是用于简化命令输入的快捷方式，使用 `unalias` 可以恢复原始命令的功能。

## 用法
基本语法如下：
```
unalias [选项] [参数]
```

## 常用选项
- `-a`：删除所有别名。
- `-m`：显示所有别名的列表。

## 常见示例
1. 删除单个别名：
   ```sh
   unalias ll
   ```

2. 删除多个别名：
   ```sh
   unalias ll la
   ```

3. 删除所有别名：
   ```sh
   unalias -a
   ```

4. 显示所有别名：
   ```sh
   unalias -m
   ```

## 提示
- 在使用 `unalias` 删除别名之前，可以使用 `alias` 命令查看当前定义的别名。
- 如果你希望在每次启动 shell 时都不加载某些别名，可以在你的配置文件（如 `.bashrc` 或 `.profile`）中删除相应的 `alias` 定义。