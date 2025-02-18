# [中文] Debian Almquist Shell (dash) rsync 用法: 文件同步和传输

## 概述
`rsync` 是一个强大的命令行工具，用于在本地和远程之间高效地同步和传输文件。它可以通过增量传输的方式，只传输变化的部分，从而节省带宽和时间。

## 用法
基本语法如下：
```bash
rsync [options] [arguments]
```

## 常用选项
- `-a`：归档模式，表示递归复制文件，并保持文件的权限、时间戳等信息。
- `-v`：详细模式，输出详细的传输过程信息。
- `-z`：在传输过程中进行压缩，以减少数据量。
- `-r`：递归复制整个目录。
- `--delete`：在目标位置删除源位置已删除的文件。
- `-e`：指定远程 shell 程序，如 `ssh`。

## 常见示例
1. **本地文件同步**
   ```bash
   rsync -av /path/to/source/ /path/to/destination/
   ```

2. **远程文件传输**
   ```bash
   rsync -avz /path/to/local/file user@remote_host:/path/to/remote/destination/
   ```

3. **从远程同步到本地**
   ```bash
   rsync -avz user@remote_host:/path/to/remote/file /path/to/local/destination/
   ```

4. **使用 SSH 进行安全传输**
   ```bash
   rsync -av -e ssh /path/to/local/file user@remote_host:/path/to/remote/destination/
   ```

5. **删除目标中不再存在的源文件**
   ```bash
   rsync -av --delete /path/to/source/ /path/to/destination/
   ```

## 提示
- 在执行大规模同步之前，可以使用 `--dry-run` 选项来预览将要执行的操作，而不实际进行文件传输。
- 使用 `-n` 或 `--dry-run` 选项可以帮助你避免意外的数据丢失。
- 定期备份重要数据时，考虑使用 `rsync` 的计划任务功能，以自动化同步过程。