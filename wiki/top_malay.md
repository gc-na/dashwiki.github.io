# [Sistem Operasi] Debian Almquist Shell (dash) top: Memantau penggunaan sumber

## Overview
Perintah `top` digunakan untuk memantau proses yang sedang berjalan dalam sistem dan memberikan maklumat tentang penggunaan sumber seperti CPU dan memori. Ia adalah alat yang berguna untuk melihat secara langsung prestasi sistem dan menguruskan proses.

## Usage
Sintaks asas untuk perintah `top` adalah seperti berikut:

```
top [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa untuk perintah `top`:

- `-d <seconds>`: Menetapkan selang masa antara kemas kini paparan.
- `-n <number>`: Menentukan bilangan kemas kini yang akan ditunjukkan sebelum keluar.
- `-b`: Menjalankan `top` dalam mod batch, berguna untuk pengeluaran ke fail.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan perintah `top`:

1. Menjalankan `top` dengan kemas kini setiap 3 saat:
   ```bash
   top -d 3
   ```

2. Menjalankan `top` dan keluar selepas 5 kemas kini:
   ```bash
   top -n 5
   ```

3. Menjalankan `top` dalam mod batch dan menyimpan output ke dalam fail:
   ```bash
   top -b -n 1 > output.txt
   ```

## Tips
- Gunakan `q` untuk keluar dari paparan `top`.
- Tekan `h` dalam `top` untuk mendapatkan bantuan tentang pintasan dan fungsi lain.
- Perhatikan proses yang menggunakan CPU dan memori yang tinggi untuk mengesan masalah prestasi.