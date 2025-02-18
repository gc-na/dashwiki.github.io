# [Sistem Operasi] Debian Almquist Shell (dash) bzip2: Mengompres dan mendekompres fail

## Overview
Perintah `bzip2` digunakan untuk mengompres dan mendekompres fail menggunakan algoritma bzip2. Ia sangat berkesan dalam mengurangkan saiz fail, menjadikannya berguna untuk penyimpanan dan pemindahan data.

## Usage
Berikut adalah sintaks asas bagi perintah `bzip2`:

```
bzip2 [options] [arguments]
```

## Common Options
- `-d`, `--decompress`: Menggunakan pilihan ini untuk mendekompres fail.
- `-k`, `--keep`: Menyimpan fail asal selepas pengompresan.
- `-f`, `--force`: Memaksa pengompresan walaupun fail dengan nama yang sama sudah ada.
- `-v`, `--verbose`: Menunjukkan maklumat terperinci semasa proses pengompresan atau pendekompresan.

## Common Examples
1. **Mengompres fail**:
   ```bash
   bzip2 fail.txt
   ```
   Ini akan menghasilkan fail `fail.txt.bz2` dan memadamkan `fail.txt`.

2. **Mendekompres fail**:
   ```bash
   bzip2 -d fail.txt.bz2
   ```
   Ini akan mengembalikan `fail.txt` dan memadamkan `fail.txt.bz2`.

3. **Mengompres fail tanpa memadam fail asal**:
   ```bash
   bzip2 -k fail.txt
   ```
   Ini akan menghasilkan `fail.txt.bz2` tetapi mengekalkan `fail.txt`.

4. **Menggunakan pilihan verbose**:
   ```bash
   bzip2 -v fail.txt
   ```
   Ini akan menunjukkan maklumat tentang proses pengompresan.

## Tips
- Sentiasa gunakan pilihan `-k` jika anda ingin mengekalkan fail asal semasa pengompresan.
- Untuk mengompres banyak fail sekaligus, anda boleh menggunakan wildcard. Contohnya:
  ```bash
  bzip2 *.txt
  ```
- Pastikan anda mempunyai ruang yang cukup pada disk untuk menyimpan fail yang telah dikompres.