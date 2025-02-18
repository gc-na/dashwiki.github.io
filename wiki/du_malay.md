# [Debian] Debian Almquist Shell (dash) du: Mengira penggunaan ruang disk

## Overview
Perintah `du` (disk usage) digunakan untuk mengira dan melaporkan penggunaan ruang disk bagi fail dan direktori dalam sistem fail. Ia membantu pengguna memahami berapa banyak ruang yang digunakan oleh fail-fail tertentu dan membantu dalam pengurusan ruang disk.

## Usage
Sintaks asas bagi perintah `du` adalah seperti berikut:

```bash
du [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan umum untuk `du` beserta penjelasan ringkas:

- `-h`: Menunjukkan saiz dalam format yang mudah dibaca (contohnya, KB, MB).
- `-s`: Menunjukkan jumlah penggunaan ruang untuk setiap argumen secara ringkas.
- `-a`: Menunjukkan penggunaan ruang untuk semua fail, bukan hanya direktori.
- `-c`: Menjumlahkan semua penggunaan ruang dan memberikan total di akhir.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `du`:

1. Mengira penggunaan ruang untuk direktori semasa:
   ```bash
   du
   ```

2. Menunjukkan penggunaan ruang dalam format yang mudah dibaca:
   ```bash
   du -h
   ```

3. Mengira penggunaan ruang untuk direktori tertentu:
   ```bash
   du /path/to/directory
   ```

4. Menunjukkan jumlah penggunaan ruang untuk setiap subdirektori:
   ```bash
   du -h --max-depth=1
   ```

5. Menjumlahkan penggunaan ruang untuk semua fail dan direktori dalam direktori semasa:
   ```bash
   du -c -h
   ```

## Tips
- Gunakan pilihan `-h` untuk memudahkan pembacaan hasil, terutamanya bagi direktori yang besar.
- Pilihan `-s` berguna untuk mendapatkan ringkasan penggunaan ruang tanpa melihat setiap subdirektori.
- Jika anda ingin melihat penggunaan ruang untuk semua fail, gunakan pilihan `-a` untuk mendapatkan maklumat yang lebih terperinci.