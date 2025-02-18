# [Sistem Operasi] Debian Almquist Shell (dash) expr Penggunaan: [mengira ekspresi]

## Overview
Perintah `expr` digunakan dalam shell untuk mengira nilai ekspresi. Ia membolehkan pengguna melakukan operasi matematik, membandingkan nilai, dan memanipulasi string.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `expr`:

```bash
expr [options] [arguments]
```

## Common Options
- `+` : Menjumlahkan dua nombor.
- `-` : Mengurangkan nombor kedua daripada nombor pertama.
- `*` : Mengalikan dua nombor.
- `/` : Membahagikan nombor pertama dengan nombor kedua.
- `%` : Mengira baki pembahagian antara dua nombor.
- `=` : Membandingkan dua nilai untuk kesamaan.
- `!=` : Membandingkan dua nilai untuk ketidaksamaan.

## Common Examples
Berikut adalah beberapa contoh penggunaan `expr`:

1. **Menjumlahkan dua nombor:**
   ```bash
   expr 5 + 3
   ```
   Output: `8`

2. **Mengurangkan nombor:**
   ```bash
   expr 10 - 4
   ```
   Output: `6`

3. **Mengalikan nombor:**
   ```bash
   expr 7 \* 6
   ```
   Output: `42`

4. **Membahagikan nombor:**
   ```bash
   expr 20 / 4
   ```
   Output: `5`

5. **Mengira baki pembahagian:**
   ```bash
   expr 10 % 3
   ```
   Output: `1`

6. **Membandingkan dua nilai:**
   ```bash
   expr 5 = 5
   ```
   Output: `1` (benar)

## Tips
- Sentiasa gunakan tanda `\` sebelum `*` untuk mengelakkan masalah dengan shell.
- Gunakan tanda kurung untuk mengelompokkan operasi jika perlu.
- `expr` hanya mengembalikan nilai integer, jadi pastikan input anda adalah nombor.