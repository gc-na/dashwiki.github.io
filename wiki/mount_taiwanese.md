# [台灣] Debian Almquist Shell (dash) mount 用法: 挂載檔案系統

## Overview
`mount` 命令用於將檔案系統掛載到指定的目錄上，使得使用者可以訪問該檔案系統中的檔案和資料夾。

## Usage
基本語法如下：
```
mount [options] [arguments]
```

## Common Options
- `-t type`：指定檔案系統的類型，例如 `ext4`、`ntfs` 等。
- `-o options`：指定掛載選項，如 `ro`（只讀）、`rw`（讀寫）等。
- `-a`：掛載 `/etc/fstab` 中列出的所有檔案系統。
- `-r`：以只讀模式掛載檔案系統。

## Common Examples
以下是一些常見的使用範例：

1. **掛載一個 ext4 檔案系統**
   ```sh
   mount -t ext4 /dev/sda1 /mnt/mydisk
   ```

2. **以只讀模式掛載一個 NTFS 檔案系統**
   ```sh
   mount -t ntfs -o ro /dev/sdb1 /mnt/myntfs
   ```

3. **掛載所有在 /etc/fstab 中定義的檔案系統**
   ```sh
   mount -a
   ```

4. **掛載一個 ISO 檔案**
   ```sh
   mount -o loop /path/to/image.iso /mnt/iso
   ```

## Tips
- 確保在掛載檔案系統之前，目錄已經存在。
- 使用 `umount` 命令來卸載已掛載的檔案系統。
- 檢查 `/etc/fstab` 文件，以便自動掛載檔案系統，這樣在啟動時會自動掛載。