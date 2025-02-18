# [中文] Debian Almquist Shell (dash) getopts 用法: 解析命令行选项

## 概述
`getopts` 命令用于解析命令行选项，使得脚本能够处理用户输入的参数。它可以帮助开发者轻松地管理和验证脚本中的选项和参数。

## 用法
基本语法如下：
```sh
getopts [options] [arguments]
```

## 常用选项
- `-a`：用于指定选项的字母。
- `-n`：用于指定脚本的名称。
- `-o`：用于设置选项的短格式。

## 常见示例
以下是一些使用 `getopts` 的实际示例：

### 示例 1：基本选项解析
```sh
#!/bin/sh
while getopts "ab:c:" opt; do
  case $opt in
    a)
      echo "Option A selected"
      ;;
    b)
      echo "Option B with argument: $OPTARG"
      ;;
    c)
      echo "Option C with argument: $OPTARG"
      ;;
    *)
      echo "Invalid option"
      ;;
  esac
done
```

### 示例 2：处理多个选项
```sh
#!/bin/sh
while getopts "x:y:z" opt; do
  case $opt in
    x)
      echo "Option X with argument: $OPTARG"
      ;;
    y)
      echo "Option Y with argument: $OPTARG"
      ;;
    z)
      echo "Option Z selected"
      ;;
    *)
      echo "Invalid option"
      ;;
  esac
done
```

### 示例 3：默认值处理
```sh
#!/bin/sh
while getopts "f:" opt; do
  case $opt in
    f)
      file=$OPTARG
      ;;
    *)
      file="default.txt"
      ;;
  esac
done
echo "Using file: $file"
```

## 提示
- 确保在使用 `getopts` 时，选项后面跟着冒号（:）表示该选项需要参数。
- 使用 `OPTARG` 变量来获取当前选项的参数值。
- 在处理选项时，使用 `case` 语句可以提高代码的可读性和可维护性。