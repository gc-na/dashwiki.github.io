# [Hệ điều hành] Debian Almquist Shell (dash) cd: Chuyển đổi thư mục làm việc

## Overview
Lệnh `cd` (change directory) trong shell cho phép người dùng chuyển đổi giữa các thư mục trong hệ thống tệp. Khi bạn sử dụng lệnh này, bạn có thể điều hướng đến thư mục mà bạn muốn làm việc.

## Usage
Cú pháp cơ bản của lệnh `cd` như sau:
```
cd [options] [arguments]
```

## Common Options
- `-`: Quay lại thư mục trước đó.
- `..`: Chuyển đến thư mục cha của thư mục hiện tại.
- `~`: Chuyển đến thư mục chính của người dùng.

## Common Examples
- Chuyển đến thư mục con có tên "documents":
  ```sh
  cd documents
  ```

- Quay lại thư mục cha:
  ```sh
  cd ..
  ```

- Quay lại thư mục trước đó:
  ```sh
  cd -
  ```

- Chuyển đến thư mục chính của người dùng:
  ```sh
  cd ~
  ```

## Tips
- Sử dụng `cd -` để nhanh chóng quay lại thư mục trước đó mà bạn đã làm việc.
- Bạn có thể sử dụng phím Tab để tự động hoàn thành tên thư mục, giúp tiết kiệm thời gian và giảm lỗi chính tả.
- Để kiểm tra thư mục hiện tại, bạn có thể sử dụng lệnh `pwd` sau khi chuyển đổi thư mục.