# [Sistem Operasi] Debian Almquist Shell (dash) gzip Penggunaan: Memampatkan fail

## Overview
Perintah `gzip` digunakan untuk memampatkan fail menggunakan algoritma pemampatan Deflate. Ia sangat berguna untuk mengurangkan saiz fail, menjadikannya lebih mudah untuk disimpan atau dihantar melalui rangkaian.

## Usage
Sintaks asas untuk menggunakan perintah `gzip` adalah seperti berikut:

```bash
gzip [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa yang boleh digunakan dengan `gzip`:

- `-d` atau `--decompress`: Menguraikan fail yang telah dimampatkan.
- `-k` atau `--keep`: Menyimpan fail asal selepas pemampatan.
- `-v` atau `--verbose`: Menunjukkan maklumat terperinci semasa pemampatan.
- `-f` atau `--force`: Memaksa pemampatan walaupun fail dengan nama yang sama sudah wujud.

## Common Examples
Berikut adalah beberapa contoh penggunaan `gzip`:

1. Memampatkan fail:
   ```bash
   gzip fail.txt
   ```

2. Menguraikan fail yang telah dimampatkan:
   ```bash
   gzip -d fail.txt.gz
   ```

3. Menyimpan fail asal semasa memampatkan:
   ```bash
   gzip -k fail.txt
   ```

4. Memampatkan fail dan menunjukkan maklumat terperinci:
   ```bash
   gzip -v fail.txt
   ```

## Tips
- Sentiasa gunakan pilihan `-k` jika anda ingin mengekalkan salinan asal fail.
- Untuk memampatkan banyak fail sekaligus, anda boleh menggunakan wildcard, contohnya `gzip *.txt`.
- Pastikan anda mempunyai ruang yang mencukupi pada sistem anda sebelum memampatkan fail besar, kerana `gzip` memerlukan ruang tambahan untuk fail sementara.