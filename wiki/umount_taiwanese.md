# [台灣] Debian Almquist Shell (dash) umount 使用方法: 卸載檔案系統

## Overview
`umount` 命令用於卸載已掛載的檔案系統。當你不再需要訪問某個檔案系統時，使用此命令可以安全地將其從系統中移除，確保資料的完整性。

## Usage
基本語法如下：
```
umount [選項] [參數]
```

## Common Options
- `-a`：卸載所有已掛載的檔案系統。
- `-r`：如果卸載失敗，則以只讀模式重新掛載。
- `-f`：強制卸載，即使檔案系統忙碌。
- `-l`：延遲卸載，立即返回但在系統空閒時卸載。

## Common Examples
1. 卸載特定的檔案系統：
   ```bash
   umount /mnt/mydrive
   ```

2. 卸載所有檔案系統：
   ```bash
   umount -a
   ```

3. 強制卸載檔案系統：
   ```bash
   umount -f /mnt/mydrive
   ```

4. 延遲卸載檔案系統：
   ```bash
   umount -l /mnt/mydrive
   ```

## Tips
- 在卸載檔案系統之前，確保沒有任何程序正在使用該檔案系統。
- 使用 `lsof` 命令檢查哪些進程正在使用檔案系統。
- 在卸載之前，最好先備份重要資料，以防資料遺失。