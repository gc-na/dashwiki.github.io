# [台灣] Debian Almquist Shell (dash) cal 使用法: 顯示日曆

## Overview
`cal` 命令用來顯示日曆，讓使用者可以快速查看特定月份或年份的日曆。

## Usage
基本語法如下：
```
cal [options] [arguments]
```

## Common Options
- `-m` : 顯示當前月份的日曆。
- `-y` : 顯示整個年份的日曆。
- `-3` : 顯示當前月份及前後各一個月的日曆。
- `-j` : 顯示 Julian 日期。

## Common Examples
- 顯示當前月份的日曆：
  ```bash
  cal
  ```

- 顯示特定月份（例如2023年10月）的日曆：
  ```bash
  cal 10 2023
  ```

- 顯示整個2023年的日曆：
  ```bash
  cal -y 2023
  ```

- 顯示當前月份及前後各一個月的日曆：
  ```bash
  cal -3
  ```

- 顯示2023年1月的 Julian 日期：
  ```bash
  cal -j 1 2023
  ```

## Tips
- 使用 `cal` 時，搭配 `-m` 可以快速查看當前月份的日曆。
- 若想要查看整個年份的計畫，使用 `-y` 是個好選擇。
- 可以將 `cal` 命令與其他命令結合使用，例如使用管道將輸出傳遞給 `less` 來方便瀏覽。