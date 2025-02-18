# [Sistem Operasi] Debian Almquist Shell (dash) watch penggunaan: Memantau perintah secara berkala

## Overview
Perintah `watch` digunakan untuk menjalankan perintah tertentu secara berkala dan memaparkan outputnya. Ini berguna untuk memantau perubahan dalam hasil perintah tanpa perlu menjalankannya secara manual berulang kali.

## Usage
Sintaks asas untuk perintah `watch` adalah seperti berikut:

```
watch [options] [arguments]
```

## Common Options
Berikut adalah pilihan umum untuk `watch` beserta penjelasan ringkas:

- `-n, --interval`: Menetapkan selang waktu (dalam saat) antara setiap pengulangan perintah.
- `-d, --differences`: Menyoroti perubahan antara output yang berbeza.
- `-t, --no-title`: Menghilangkan tajuk yang menunjukkan perintah yang sedang dijalankan.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `watch`:

1. Memantau penggunaan CPU setiap 2 saat:
   ```bash
   watch -n 2 mpstat
   ```

2. Memantau perubahan dalam direktori semasa:
   ```bash
   watch ls -l
   ```

3. Memantau status perkhidmatan tertentu:
   ```bash
   watch systemctl status apache2
   ```

4. Menyoroti perubahan dalam output perintah `df`:
   ```bash
   watch -d df -h
   ```

## Tips
- Gunakan pilihan `-n` untuk menyesuaikan selang waktu sesuai keperluan anda.
- Untuk memudahkan pembacaan, gunakan pilihan `-d` untuk menyoroti perubahan yang berlaku.
- Jika anda tidak memerlukan tajuk, gunakan pilihan `-t` untuk menjadikan output lebih bersih.