# [Sistem Operasi] Debian Almquist Shell (dash) renice: Mengubah keutamaan proses

## Overview
Perintah `renice` digunakan untuk mengubah keutamaan proses yang sedang berjalan di sistem. Dengan mengubah keutamaan ini, pengguna dapat mengawal berapa banyak sumber daya CPU yang diberikan kepada proses tertentu, yang boleh membantu dalam pengurusan prestasi sistem.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `renice`:

```bash
renice [options] [arguments]
```

## Common Options
- `-n, --priority <n>`: Menetapkan keutamaan baru untuk proses. Nilai `n` boleh antara -20 (keutamaan tertinggi) hingga 19 (keutamaan terendah).
- `-p, --pid <pid>`: Menentukan ID proses yang ingin diubah keutamaannya.
- `-g, --pgroup <pgrp>`: Mengubah keutamaan semua proses dalam kumpulan proses tertentu.
- `-u, --user <user>`: Mengubah keutamaan semua proses yang dimiliki oleh pengguna tertentu.

## Common Examples
1. Mengubah keutamaan proses dengan ID 1234 kepada 10:
   ```bash
   renice -n 10 -p 1234
   ```

2. Mengubah keutamaan semua proses milik pengguna "john" kepada -5:
   ```bash
   renice -n -5 -u john
   ```

3. Mengubah keutamaan semua proses dalam kumpulan proses dengan ID 5678 kepada 0:
   ```bash
   renice -n 0 -g 5678
   ```

4. Memeriksa keutamaan proses tertentu sebelum dan selepas mengubahnya:
   ```bash
   ps -o pid,ni,comm
   renice -n 5 -p 1234
   ps -o pid,ni,comm
   ```

## Tips
- Sentiasa semak keutamaan proses sebelum dan selepas menggunakan `renice` untuk memastikan perubahan yang diingini.
- Gunakan nilai keutamaan yang sesuai; mengatur keutamaan terlalu tinggi atau rendah boleh menyebabkan masalah prestasi.
- Hanya pengguna dengan hak istimewa yang boleh mengubah keutamaan proses yang dimiliki oleh pengguna lain.