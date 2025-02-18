# [中文] Debian Almquist Shell (dash) shift 用法: 改变位置参数

## 概述
`shift` 命令用于在脚本中改变位置参数。它通过将所有位置参数向左移动来实现这一点，使得 `$1` 变为 `$2`，`$2` 变为 `$3`，依此类推。这样可以方便地处理参数列表，尤其是在循环或条件语句中。

## 用法
基本语法如下：
```sh
shift [n]
```
其中 `n` 是要移动的位置参数的数量，默认为 1。

## 常用选项
- `n`：指定要移动的位置参数的数量。如果不提供，默认移动 1 个位置参数。

## 常见示例
以下是一些常见的 `shift` 命令示例：

### 示例 1: 默认移动
```sh
#!/bin/dash
set -- one two three
echo "Before shift: $1"  # 输出: one
shift
echo "After shift: $1"   # 输出: two
```

### 示例 2: 移动多个位置参数
```sh
#!/bin/dash
set -- one two three four
echo "Before shift: $1"  # 输出: one
shift 2
echo "After shift: $1"   # 输出: three
```

### 示例 3: 在循环中使用
```sh
#!/bin/dash
set -- apple banana cherry
while [ "$#" -gt 0 ]; do
    echo "Current fruit: $1"
    shift
done
```

## 提示
- 在使用 `shift` 时，请确保在脚本中有足够的参数可供移动，以避免出现未定义的变量。
- 可以结合 `getopts` 命令使用 `shift`，以处理命令行选项和参数。
- 在处理大量参数时，合理使用 `shift` 可以使代码更加简洁和易于维护。