# [Sistem Operasi] Debian Almquist Shell (dash) killall <Menghentikan proses>: Menghentikan semua proses dengan nama tertentu

## Overview
Perintah `killall` digunakan untuk menghentikan semua proses yang berjalan dengan nama tertentu. Ini sangat berguna ketika Anda ingin menghentikan beberapa instance dari aplikasi yang sama tanpa harus mencari dan menghentikan setiap proses secara manual.

## Usage
Berikut adalah sintaks dasar dari perintah `killall`:

```bash
killall [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan `killall`:

- `-u <user>`: Hentikan proses yang berjalan oleh pengguna tertentu.
- `-s <signal>`: Kirim sinyal tertentu ke proses (default adalah SIGTERM).
- `-I`: Abaikan huruf besar/kecil saat mencocokkan nama proses.

## Common Examples
Berikut adalah beberapa contoh penggunaan `killall`:

1. Menghentikan semua proses dengan nama "firefox":
   ```bash
   killall firefox
   ```

2. Menghentikan semua proses "gedit" dengan mengirimkan sinyal SIGKILL:
   ```bash
   killall -s SIGKILL gedit
   ```

3. Menghentikan semua proses "python" yang dijalankan oleh pengguna "user1":
   ```bash
   killall -u user1 python
   ```

4. Menghentikan semua proses "myapp" tanpa memperhatikan huruf besar/kecil:
   ```bash
   killall -I myapp
   ```

## Tips
- Selalu pastikan untuk memeriksa proses yang akan dihentikan agar tidak menghentikan proses penting secara tidak sengaja.
- Gunakan opsi `-s` untuk mengirim sinyal yang sesuai jika proses tidak merespons sinyal default.
- Anda dapat menggunakan perintah `pgrep` untuk mencari tahu proses mana yang sedang berjalan sebelum menggunakan `killall`.