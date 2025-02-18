# [Sistem Operasi] Debian Almquist Shell (dash) cp: [menyalin file dan direktori]

## Overview
Perintah `cp` digunakan untuk menyalin file dan direktori dalam sistem operasi berbasis Unix, termasuk Debian Almquist Shell (dash). Dengan perintah ini, Anda dapat membuat salinan dari file atau direktori yang ada ke lokasi yang diinginkan.

## Usage
Berikut adalah sintaks dasar dari perintah `cp`:

```bash
cp [options] [source] [destination]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan perintah `cp`:

- `-r`: Menyalin direktori secara rekursif.
- `-i`: Meminta konfirmasi sebelum menimpa file yang ada.
- `-u`: Menyalin hanya jika file sumber lebih baru daripada file tujuan atau jika file tujuan tidak ada.
- `-v`: Menampilkan informasi tentang file yang sedang disalin.

## Common Examples

1. Menyalin file tunggal:
   ```bash
   cp file1.txt file2.txt
   ```

2. Menyalin direktori secara rekursif:
   ```bash
   cp -r direktori1/ direktori2/
   ```

3. Menyalin file dengan konfirmasi:
   ```bash
   cp -i file1.txt file2.txt
   ```

4. Menyalin file hanya jika lebih baru:
   ```bash
   cp -u file1.txt file2.txt
   ```

5. Menyalin file sambil menampilkan proses:
   ```bash
   cp -v file1.txt file2.txt
   ```

## Tips
- Selalu gunakan opsi `-i` jika Anda tidak ingin menimpa file yang sudah ada tanpa konfirmasi.
- Saat menyalin direktori, pastikan untuk menggunakan opsi `-r` agar semua konten di dalam direktori juga disalin.
- Gunakan opsi `-v` untuk memantau proses penyalinan, terutama saat menyalin banyak file.