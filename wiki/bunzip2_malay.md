# [Sistem Operasi] Debian Almquist Shell (dash) bunzip2: Mengurangkan saiz fail bzip2

## Overview
Perintah `bunzip2` digunakan untuk mengekstrak fail yang telah dimampatkan menggunakan algoritma bzip2. Ia mengembalikan fail kepada bentuk asalnya selepas pemampatan.

## Usage
Sintaks asas untuk menggunakan `bunzip2` adalah seperti berikut:

```
bunzip2 [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa untuk `bunzip2`:

- `-k`: Menyimpan fail asal selepas mengekstrak.
- `-f`: Memaksa pengekstrakan walaupun fail sasaran sudah ada.
- `-v`: Menunjukkan maklumat terperinci semasa proses pengekstrakan.

## Common Examples
Berikut adalah beberapa contoh penggunaan `bunzip2`:

1. Mengekstrak fail `file.bz2`:
   ```bash
   bunzip2 file.bz2
   ```

2. Mengekstrak fail dan menyimpan fail asal:
   ```bash
   bunzip2 -k file.bz2
   ```

3. Memaksa pengekstrakan walaupun fail `file` sudah ada:
   ```bash
   bunzip2 -f file.bz2
   ```

4. Menunjukkan maklumat terperinci semasa pengekstrakan:
   ```bash
   bunzip2 -v file.bz2
   ```

## Tips
- Sentiasa semak ruang simpanan sebelum mengekstrak fail besar untuk mengelakkan masalah kekurangan ruang.
- Gunakan pilihan `-k` jika anda ingin mengekalkan fail asal untuk rujukan atau penggunaan lain.
- Jika anda bekerja dengan banyak fail, pertimbangkan untuk menggunakan pengendalian batch dengan skrip shell untuk menjimatkan masa.