# [臺灣] Debian Almquist Shell (dash) ln 使用法: 創建檔案的連結

## Overview
`ln` 命令用於在檔案系統中創建檔案的連結。這些連結可以是硬連結或符號連結，讓使用者能夠通過不同的路徑訪問相同的檔案。

## Usage
基本語法如下：
```bash
ln [options] [arguments]
```

## Common Options
- `-s`: 創建符號連結，而不是硬連結。
- `-f`: 強制覆蓋已存在的檔案連結。
- `-n`: 在創建連結時不跟隨目標檔案的連結。
- `-v`: 顯示詳細的操作過程。

## Common Examples
1. 創建一個硬連結：
   ```bash
   ln original.txt link_to_original.txt
   ```

2. 創建一個符號連結：
   ```bash
   ln -s original.txt symlink_to_original.txt
   ```

3. 強制覆蓋已存在的連結：
   ```bash
   ln -sf original.txt link_to_original.txt
   ```

4. 創建符號連結並顯示詳細信息：
   ```bash
   ln -sv original.txt symlink_to_original.txt
   ```

## Tips
- 使用符號連結時，請確保目標檔案的路徑正確，否則連結將無法正常工作。
- 硬連結無法跨不同的檔案系統，因此在使用時需注意檔案系統的限制。
- 使用 `-v` 選項可以幫助你了解命令的執行過程，特別是在批量創建連結時。