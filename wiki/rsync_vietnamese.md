# [Hệ điều hành Debian] Debian Almquist Shell (dash) rsync: [sao chép và đồng bộ hóa tệp]

## Tổng quan
Lệnh `rsync` là một công cụ mạnh mẽ dùng để sao chép và đồng bộ hóa tệp và thư mục giữa hai vị trí, có thể là trên cùng một máy hoặc giữa các máy khác nhau qua mạng. Nó rất hiệu quả trong việc chỉ sao chép các phần đã thay đổi của tệp, giúp tiết kiệm băng thông và thời gian.

## Cú pháp
Cú pháp cơ bản của lệnh `rsync` như sau:
```
rsync [tùy chọn] [đối số]
```

## Các tùy chọn phổ biến
- `-a`: Chế độ lưu trữ, sao chép tệp và thư mục cùng với các thuộc tính của chúng.
- `-v`: Hiển thị thông tin chi tiết về quá trình sao chép.
- `-z`: Nén dữ liệu trong quá trình truyền tải để tiết kiệm băng thông.
- `-r`: Sao chép thư mục một cách đệ quy.
- `--delete`: Xóa các tệp trong thư mục đích mà không còn tồn tại trong thư mục nguồn.

## Ví dụ thường gặp
- Sao chép một thư mục từ máy cục bộ đến máy chủ từ xa:
```bash
rsync -av /path/to/local/dir/ user@remote:/path/to/remote/dir/
```

- Đồng bộ hóa một thư mục từ máy chủ từ xa về máy cục bộ:
```bash
rsync -av user@remote:/path/to/remote/dir/ /path/to/local/dir/
```

- Sao chép tệp và nén dữ liệu:
```bash
rsync -avz /path/to/local/file.txt user@remote:/path/to/remote/
```

- Đồng bộ hóa và xóa tệp không còn tồn tại trong thư mục nguồn:
```bash
rsync -av --delete /path/to/local/dir/ user@remote:/path/to/remote/dir/
```

## Mẹo
- Luôn sử dụng tùy chọn `-n` (dry run) để kiểm tra những gì sẽ được sao chép trước khi thực hiện lệnh thực tế.
- Sử dụng `--progress` để theo dõi tiến trình sao chép, đặc biệt khi làm việc với các tệp lớn.
- Đảm bảo rằng bạn có quyền truy cập cần thiết trên cả hai hệ thống khi sử dụng `rsync` qua mạng.