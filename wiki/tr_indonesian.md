# [Sistem Operasi] Debian Almquist Shell (dash) tr: Mengubah karakter dalam teks

## Overview
Perintah `tr` (translate) digunakan untuk mengubah atau mengganti karakter dalam input teks. Perintah ini sangat berguna untuk memanipulasi data teks, seperti menghapus karakter tertentu atau mengganti satu karakter dengan karakter lain.

## Usage
Sintaks dasar dari perintah `tr` adalah sebagai berikut:

```bash
tr [options] [arguments]
```

## Common Options
- `-d`: Menghapus karakter yang ditentukan dari input.
- `-s`: Mengganti beberapa karakter yang berurutan dengan satu karakter.
- `-c`: Menggunakan karakter yang tidak ditentukan dalam operasi.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `tr`:

1. **Mengganti huruf kecil menjadi huruf besar:**
   ```bash
   echo "hello world" | tr 'a-z' 'A-Z'
   ```
   Output: `HELLO WORLD`

2. **Menghapus semua angka dari teks:**
   ```bash
   echo "abc123def456" | tr -d '0-9'
   ```
   Output: `abcdef`

3. **Mengganti spasi dengan garis bawah:**
   ```bash
   echo "hello world" | tr ' ' '_'
   ```
   Output: `hello_world`

4. **Mengganti beberapa spasi berurutan menjadi satu spasi:**
   ```bash
   echo "hello    world" | tr -s ' '
   ```
   Output: `hello world`

## Tips
- Selalu gunakan tanda kutip untuk menghindari kesalahan saat menggunakan karakter khusus.
- Kombinasikan `tr` dengan perintah lain menggunakan pipe (`|`) untuk memproses data lebih lanjut.
- Periksa hasil output dengan menggunakan `cat -e` untuk melihat karakter akhir baris dan spasi yang tidak terlihat.