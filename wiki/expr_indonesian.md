# [Sistem Operasi] Debian Almquist Shell (dash) expr: [menghitung ekspresi]

## Overview
Perintah `expr` dalam shell Debian Almquist (dash) digunakan untuk mengevaluasi ekspresi dan melakukan operasi aritmatika, perbandingan, dan string. Ini berguna untuk melakukan perhitungan sederhana dalam skrip shell.

## Usage
Berikut adalah sintaks dasar dari perintah `expr`:

```bash
expr [options] [arguments]
```

## Common Options
- `+` : Menjumlahkan dua angka.
- `-` : Mengurangi angka kedua dari angka pertama.
- `*` : Mengalikan dua angka.
- `/` : Membagi angka pertama dengan angka kedua.
- `%` : Menghitung sisa pembagian dari dua angka.
- `=` : Memeriksa kesetaraan antara dua nilai.
- `!=` : Memeriksa ketidaksetaraan antara dua nilai.

## Common Examples
Berikut adalah beberapa contoh praktis penggunaan `expr`:

1. Menjumlahkan dua angka:
   ```bash
   expr 5 + 3
   ```
   Output: `8`

2. Mengurangi angka:
   ```bash
   expr 10 - 4
   ```
   Output: `6`

3. Mengalikan dua angka:
   ```bash
   expr 7 \* 6
   ```
   Output: `42`

4. Membagi angka:
   ```bash
   expr 20 / 4
   ```
   Output: `5`

5. Menghitung sisa pembagian:
   ```bash
   expr 10 % 3
   ```
   Output: `1`

6. Memeriksa kesetaraan:
   ```bash
   expr 5 = 5
   ```
   Output: `1` (true)

7. Memeriksa ketidaksetaraan:
   ```bash
   expr 5 != 3
   ```
   Output: `1` (true)

## Tips
- Selalu gunakan tanda backslash (`\`) sebelum operator `*` untuk menghindari konflik dengan shell.
- Gunakan tanda kurung untuk mengelompokkan ekspresi yang lebih kompleks.
- Hati-hati dengan spasi; `expr` memerlukan spasi di sekitar operator untuk berfungsi dengan benar.