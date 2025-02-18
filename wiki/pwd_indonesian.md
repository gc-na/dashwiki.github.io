# [Sistem Operasi] Debian Almquist Shell (dash) pwd: Menampilkan direktori kerja saat ini

## Overview
Perintah `pwd` (print working directory) digunakan untuk menampilkan jalur direktori kerja saat ini di dalam terminal. Ini sangat berguna untuk mengetahui lokasi Anda dalam struktur sistem file.

## Usage
Berikut adalah sintaks dasar dari perintah `pwd`:

```
pwd [options] [arguments]
```

## Common Options
- `-L`: Menampilkan jalur logis dari direktori kerja saat ini.
- `-P`: Menampilkan jalur fisik dari direktori kerja saat ini, mengabaikan symlink.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `pwd`:

1. Menampilkan direktori kerja saat ini:
   ```bash
   pwd
   ```

2. Menampilkan jalur fisik dari direktori kerja saat ini:
   ```bash
   pwd -P
   ```

3. Menampilkan jalur logis dari direktori kerja saat ini:
   ```bash
   pwd -L
   ```

## Tips
- Gunakan `pwd` secara rutin untuk memastikan Anda berada di direktori yang tepat sebelum menjalankan perintah lain.
- Kombinasikan `pwd` dengan perintah lain seperti `cd` untuk navigasi yang lebih efisien dalam sistem file.
- Ingat bahwa output dari `pwd` dapat digunakan dalam skrip untuk mengatur jalur file relatif.