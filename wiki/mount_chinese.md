# [中文] Debian Almquist Shell (dash) mount 用法: 挂载文件系统

## 概述
`mount` 命令用于将文件系统挂载到系统的目录树中，使得用户可以访问存储在该文件系统上的文件和目录。

## 用法
基本语法如下：
```
mount [options] [arguments]
```

## 常用选项
- `-t type`：指定文件系统的类型，例如 `ext4`、`ntfs` 等。
- `-o options`：指定挂载选项，如 `ro`（只读）、`rw`（读写）。
- `-a`：挂载 `/etc/fstab` 文件中列出的所有文件系统。
- `-r`：以只读模式挂载文件系统。

## 常见示例
1. 挂载一个 USB 驱动器：
   ```sh
   mount /dev/sdb1 /mnt/usb
   ```

2. 以只读模式挂载一个 ISO 文件：
   ```sh
   mount -o loop -r /path/to/image.iso /mnt/iso
   ```

3. 挂载所有在 `/etc/fstab` 中定义的文件系统：
   ```sh
   mount -a
   ```

4. 挂载一个 ext4 文件系统并指定为读写：
   ```sh
   mount -t ext4 -o rw /dev/sda1 /mnt/data
   ```

## 提示
- 确保在挂载之前目标目录存在。
- 使用 `umount` 命令卸载文件系统，以避免数据丢失。
- 检查 `/etc/fstab` 文件，以便在系统启动时自动挂载文件系统。