# [Sistem Operasi] Debian Almquist Shell (dash) uname Penggunaan: Menunjukkan maklumat sistem

## Overview
Perintah `uname` digunakan untuk menampilkan maklumat mengenai sistem operasi yang sedang berjalan. Ia memberikan informasi seperti nama kernel, versi kernel, dan jenis mesin, yang berguna untuk pemahaman lebih lanjut tentang persekitaran sistem.

## Usage
Berikut adalah sintaks asas untuk perintah `uname`:

```
uname [options] [arguments]
```

## Common Options
- `-a`: Menampilkan semua maklumat sistem.
- `-s`: Menampilkan nama kernel.
- `-n`: Menampilkan nama hos.
- `-r`: Menampilkan versi kernel.
- `-v`: Menampilkan maklumat versi kernel.
- `-m`: Menampilkan jenis mesin.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `uname`:

1. Menampilkan semua maklumat sistem:
   ```bash
   uname -a
   ```

2. Menampilkan nama kernel:
   ```bash
   uname -s
   ```

3. Menampilkan versi kernel:
   ```bash
   uname -r
   ```

4. Menampilkan nama hos:
   ```bash
   uname -n
   ```

5. Menampilkan jenis mesin:
   ```bash
   uname -m
   ```

## Tips
- Gunakan `uname -a` untuk mendapatkan gambaran keseluruhan tentang sistem anda dalam satu perintah.
- Perintah ini berguna untuk skrip automasi yang memerlukan maklumat sistem untuk pengesahan atau konfigurasi.
- Pastikan anda menjalankan perintah ini dalam terminal untuk melihat hasilnya secara langsung.