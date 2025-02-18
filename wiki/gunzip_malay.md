# [Sistem Operasi] Debian Almquist Shell (dash) gunzip: [mengekstrak fail gzip]

## Overview
Perintah `gunzip` digunakan untuk mengekstrak fail yang telah dimampatkan menggunakan format gzip. Ia adalah alat yang berguna untuk mengembalikan fail kepada bentuk asalnya, menjadikannya boleh diakses dan digunakan semula.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `gunzip`:

```
gunzip [options] [arguments]
```

## Common Options
- `-c`: Mengeluarkan hasil ke standard output tanpa mengubah fail asal.
- `-f`: Memaksa penggantian fail yang sedia ada.
- `-k`: Menyimpan fail asal selepas mengekstrak.
- `-r`: Menyokong pemprosesan secara rekursif dalam direktori.

## Common Examples
Berikut adalah beberapa contoh penggunaan `gunzip`:

1. Mengekstrak fail gzip:
   ```bash
   gunzip fail.gz
   ```

2. Mengekstrak fail gzip dan menyimpan fail asal:
   ```bash
   gunzip -k fail.gz
   ```

3. Mengeluarkan hasil ke standard output:
   ```bash
   gunzip -c fail.gz > fail.txt
   ```

4. Mengekstrak semua fail gzip dalam direktori secara rekursif:
   ```bash
   gunzip -r direktori/
   ```

## Tips
- Sentiasa buat salinan fail asal sebelum mengekstrak, terutamanya jika anda menggunakan pilihan `-f`.
- Gunakan pilihan `-k` jika anda ingin mengekalkan fail asal selepas mengekstrak.
- Untuk memeriksa sama ada fail gzip boleh diekstrak tanpa mengekstraknya, anda boleh menggunakan perintah `gzip -t fail.gz`.