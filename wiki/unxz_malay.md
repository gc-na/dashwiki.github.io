# [Sistem Operasi] Debian Almquist Shell (dash) unxz: Menyahzip fail .xz

## Overview
Perintah `unxz` digunakan untuk menyahzip fail yang mempunyai sambungan `.xz`. Ia adalah alat yang berguna untuk mengembalikan fail yang telah dimampatkan menggunakan algoritma XZ, menjadikannya lebih mudah untuk diakses dan digunakan.

## Usage
Sintaks asas untuk perintah `unxz` adalah seperti berikut:

```
unxz [options] [arguments]
```

## Common Options
- `-k`, `--keep`: Menyimpan fail asal selepas menyahzip.
- `-f`, `--force`: Memaksa penyahzip walaupun fail sasaran sudah wujud.
- `-v`, `--verbose`: Menunjukkan maklumat lebih lanjut semasa proses penyahzip.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `unxz`:

1. **Menyahzip fail .xz**:
   ```bash
   unxz fail.txt.xz
   ```

2. **Menyahzip fail dan menyimpan fail asal**:
   ```bash
   unxz -k fail.txt.xz
   ```

3. **Memaksa penyahzip walaupun fail sudah wujud**:
   ```bash
   unxz -f fail.txt.xz
   ```

4. **Menyahzip fail dengan maklumat lanjut**:
   ```bash
   unxz -v fail.txt.xz
   ```

## Tips
- Sentiasa semak sama ada fail sasaran sudah wujud sebelum menggunakan pilihan `-f` untuk mengelakkan kehilangan data.
- Gunakan pilihan `-k` jika anda ingin mengekalkan fail asal untuk rujukan masa depan.
- Untuk fail yang besar, pertimbangkan untuk menggunakan pilihan `-v` bagi memantau kemajuan proses penyahzip.