# [Sistem Operasi] Debian Almquist Shell (dash) who: Menunjukkan pengguna yang sedang log masuk

## Overview
Perintah `who` dalam shell Debian Almquist (dash) digunakan untuk menampilkan senarai pengguna yang sedang log masuk ke sistem. Ia memberikan maklumat tentang sesi pengguna, termasuk nama pengguna, terminal yang digunakan, dan waktu log masuk.

## Usage
Berikut adalah sintaks asas untuk perintah `who`:

```
who [options] [arguments]
```

## Common Options
Beberapa pilihan umum untuk perintah `who` termasuk:

- `-a`: Menunjukkan semua maklumat yang tersedia, termasuk pengguna yang tidak aktif.
- `-b`: Menunjukkan waktu terakhir sistem dimulakan.
- `-q`: Menunjukkan senarai pengguna yang sedang log masuk dan jumlah mereka.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan perintah `who`:

1. Menunjukkan semua pengguna yang sedang log masuk:
   ```bash
   who
   ```

2. Menunjukkan waktu terakhir sistem dimulakan:
   ```bash
   who -b
   ```

3. Menunjukkan senarai pengguna yang sedang log masuk dan jumlah mereka:
   ```bash
   who -q
   ```

4. Menunjukkan semua maklumat pengguna, termasuk yang tidak aktif:
   ```bash
   who -a
   ```

## Tips
- Gunakan `who` secara berkala untuk memantau sesi pengguna di sistem anda.
- Kombinasikan `who` dengan perintah lain seperti `grep` untuk mencari pengguna tertentu.
- Ingat bahawa maklumat yang dipaparkan oleh `who` mungkin berbeza bergantung kepada hak akses pengguna yang menjalankan perintah tersebut.