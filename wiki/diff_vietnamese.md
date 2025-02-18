# [Hệ điều hành] Debian Almquist Shell (dash) diff <Sử dụng tương đương>: So sánh sự khác biệt giữa các tệp

## Tổng quan
Lệnh `diff` được sử dụng để so sánh nội dung của hai tệp hoặc thư mục, giúp xác định sự khác biệt giữa chúng. Kết quả của lệnh này thường được sử dụng để xem xét các thay đổi giữa các phiên bản của tệp.

## Cách sử dụng
Cú pháp cơ bản của lệnh `diff` như sau:
```bash
diff [options] [arguments]
```

## Các tùy chọn phổ biến
- `-u`: Hiển thị kết quả theo định dạng "unified", dễ đọc hơn.
- `-i`: Bỏ qua sự khác biệt về chữ hoa và chữ thường.
- `-w`: Bỏ qua sự khác biệt về khoảng trắng.
- `-r`: So sánh các thư mục một cách đệ quy.

## Ví dụ phổ biến
Dưới đây là một số ví dụ thực tế về cách sử dụng lệnh `diff`:

1. So sánh hai tệp văn bản:
   ```bash
   diff file1.txt file2.txt
   ```

2. So sánh hai tệp và hiển thị kết quả theo định dạng "unified":
   ```bash
   diff -u file1.txt file2.txt
   ```

3. So sánh hai thư mục và hiển thị sự khác biệt giữa các tệp trong đó:
   ```bash
   diff -r dir1/ dir2/
   ```

4. So sánh hai tệp mà không phân biệt chữ hoa chữ thường:
   ```bash
   diff -i file1.txt file2.txt
   ```

## Mẹo
- Khi so sánh các tệp lớn, hãy sử dụng tùy chọn `-u` để dễ dàng nhận diện sự khác biệt.
- Nếu bạn thường xuyên làm việc với các tệp có nhiều khoảng trắng, hãy sử dụng tùy chọn `-w` để bỏ qua những khác biệt không cần thiết.
- Để lưu kết quả so sánh vào một tệp, bạn có thể sử dụng toán tử chuyển hướng:
  ```bash
  diff file1.txt file2.txt > result.txt
  ```