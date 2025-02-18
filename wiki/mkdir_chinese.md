# [中文] Debian Almquist Shell (dash) mkdir 用法: 创建目录

## 概述
`mkdir` 命令用于在文件系统中创建新目录。它是一个非常基本但重要的命令，常用于组织文件和目录结构。

## 用法
基本语法如下：
```bash
mkdir [选项] [参数]
```

## 常用选项
- `-p`：创建多级目录，如果上级目录不存在，则一并创建。
- `-m`：设置新目录的权限模式。
- `--help`：显示帮助信息。

## 常见示例
1. 创建一个新目录：
   ```bash
   mkdir my_directory
   ```

2. 创建多个目录：
   ```bash
   mkdir dir1 dir2 dir3
   ```

3. 创建多级目录：
   ```bash
   mkdir -p parent/child/grandchild
   ```

4. 设置权限模式创建目录：
   ```bash
   mkdir -m 755 my_secure_directory
   ```

## 提示
- 使用 `-p` 选项可以避免因上级目录不存在而导致的错误。
- 在创建目录时，确保你有足够的权限，否则可能会遇到权限拒绝的错误。
- 定期整理和清理不必要的目录，有助于保持文件系统的整洁。