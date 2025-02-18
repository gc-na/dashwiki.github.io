# [Debian] Debian Almquist Shell (dash) xz: Mengompres dan mendekompres fail

## Overview
Perintah `xz` digunakan untuk mengompres dan mendekompres fail menggunakan algoritma kompresi LZMA. Ia sangat berkesan dalam mengurangkan saiz fail, menjadikannya berguna untuk penyimpanan dan pemindahan data.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `xz`:

```bash
xz [options] [arguments]
```

## Common Options
- `-d`, `--decompress`: Mendekompres fail.
- `-k`, `--keep`: Menyimpan fail asal selepas mengompres.
- `-f`, `--force`: Memaksa penggantian fail tanpa meminta pengesahan.
- `-9`: Menggunakan tahap kompresi maksimum.
- `-t`, `--test`: Menguji fail terkompresi untuk memastikan ia tidak rosak.

## Common Examples
1. **Mengompres fail**:
   ```bash
   xz myfile.txt
   ```
   Ini akan menghasilkan fail `myfile.txt.xz` dan menghapuskan `myfile.txt`.

2. **Mendekompres fail**:
   ```bash
   xz -d myfile.txt.xz
   ```
   Ini akan mengembalikan fail asal `myfile.txt` dan menghapuskan `myfile.txt.xz`.

3. **Mengompres fail tetapi menyimpan fail asal**:
   ```bash
   xz -k myfile.txt
   ```
   Ini akan menghasilkan `myfile.txt.xz` tetapi tetap menyimpan `myfile.txt`.

4. **Menggunakan tahap kompresi maksimum**:
   ```bash
   xz -9 myfile.txt
   ```
   Ini akan mengompres `myfile.txt` dengan tahap kompresi tertinggi.

5. **Menguji fail terkompresi**:
   ```bash
   xz -t myfile.txt.xz
   ```
   Ini akan memeriksa sama ada `myfile.txt.xz` tidak rosak.

## Tips
- Gunakan pilihan `-k` jika anda ingin menyimpan fail asal semasa mengompres.
- Untuk fail yang sangat besar, pertimbangkan untuk menggunakan pilihan `-9` untuk mendapatkan saiz fail yang lebih kecil, walaupun ia mungkin mengambil masa lebih lama untuk mengompres.
- Sentiasa uji fail terkompresi selepas pemindahan untuk memastikan integriti data.