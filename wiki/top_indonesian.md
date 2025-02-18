# [Sistem Operasi] Debian Almquist Shell (dash) top: Menampilkan proses yang berjalan

## Overview
Perintah `top` digunakan untuk menampilkan informasi tentang proses yang sedang berjalan di sistem secara real-time. Ini memberikan gambaran umum tentang penggunaan CPU, memori, dan sumber daya lainnya oleh berbagai proses.

## Usage
Sintaks dasar dari perintah `top` adalah sebagai berikut:

```
top [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan perintah `top`:

- `-d <seconds>`: Mengatur interval pembaruan tampilan dalam detik.
- `-p <pid>`: Menampilkan hanya proses dengan ID tertentu.
- `-u <user>`: Menampilkan hanya proses yang dijalankan oleh pengguna tertentu.

## Common Examples
Berikut adalah beberapa contoh praktis penggunaan perintah `top`:

1. Menjalankan `top` dengan pembaruan setiap 2 detik:
   ```bash
   top -d 2
   ```

2. Menampilkan proses untuk pengguna tertentu:
   ```bash
   top -u username
   ```

3. Menampilkan proses dengan ID tertentu:
   ```bash
   top -p 1234
   ```

## Tips
- Gunakan tombol `h` saat dalam tampilan `top` untuk mendapatkan bantuan tentang cara menggunakan perintah ini.
- Tekan `q` untuk keluar dari tampilan `top`.
- Anda dapat mengurutkan proses berdasarkan penggunaan CPU atau memori dengan menekan tombol yang sesuai saat dalam tampilan `top`.