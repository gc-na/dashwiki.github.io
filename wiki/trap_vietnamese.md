# [Hệ điều hành] Debian Almquist Shell (dash) trap: [quản lý tín hiệu]

## Overview
Lệnh `trap` trong shell được sử dụng để xử lý các tín hiệu và sự kiện trong quá trình thực thi của một script. Nó cho phép người dùng chỉ định các hành động cụ thể khi nhận được các tín hiệu nhất định, giúp quản lý quá trình một cách hiệu quả hơn.

## Usage
Cú pháp cơ bản của lệnh `trap` như sau:
```sh
trap [options] [arguments]
```

## Common Options
- `SIGNAL`: Tín hiệu mà bạn muốn xử lý (ví dụ: `SIGINT`, `SIGTERM`).
- `COMMAND`: Lệnh hoặc hành động mà bạn muốn thực hiện khi tín hiệu được nhận.

## Common Examples
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `trap`:

### Ví dụ 1: Bắt tín hiệu SIGINT
```sh
trap 'echo "Tín hiệu SIGINT đã được nhận!"' SIGINT
while true; do
    sleep 1
done
```
Trong ví dụ này, khi người dùng nhấn `Ctrl+C`, thông báo sẽ được in ra.

### Ví dụ 2: Dọn dẹp trước khi thoát
```sh
trap 'rm -f /tmp/tempfile; echo "Đã dọn dẹp!"' EXIT
touch /tmp/tempfile
```
Lệnh này sẽ xóa tệp `/tmp/tempfile` khi script kết thúc, bất kể lý do kết thúc.

### Ví dụ 3: Bắt nhiều tín hiệu
```sh
trap 'echo "Tín hiệu nhận!"' SIGINT SIGTERM
```
Trong trường hợp này, cả hai tín hiệu `SIGINT` và `SIGTERM` đều sẽ kích hoạt hành động in ra thông báo.

## Tips
- Sử dụng `trap` để đảm bảo rằng các tài nguyên được dọn dẹp đúng cách khi script kết thúc.
- Hãy cẩn thận với các tín hiệu mà bạn chọn để bắt, vì việc xử lý không đúng có thể gây ra hành vi không mong muốn trong script.
- Kiểm tra các tín hiệu có sẵn trên hệ thống của bạn để biết thêm thông tin về những gì có thể được xử lý.