# [Sistem Operasi] Debian Almquist Shell (dash) ps Penggunaan: [menunjukkan proses yang sedang berjalan]

## Overview
Perintah `ps` dalam shell Debian Almquist (dash) digunakan untuk menampilkan senarai proses yang sedang berjalan pada sistem. Ia memberikan maklumat tentang proses-proses ini, termasuk ID proses (PID), status, dan penggunaan sumber.

## Usage
Berikut adalah sintaks asas untuk perintah `ps`:

```bash
ps [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan umum untuk `ps` beserta penjelasan ringkas:

- `-e` : Menunjukkan semua proses yang sedang berjalan.
- `-f` : Menampilkan proses dalam format penuh, termasuk maklumat tambahan seperti pengguna dan waktu.
- `-u [user]` : Menunjukkan proses yang dimiliki oleh pengguna tertentu.
- `-p [pid]` : Menunjukkan proses dengan ID proses tertentu.
- `-aux` : Menampilkan semua proses dengan maklumat lengkap.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan perintah `ps`:

1. Menampilkan semua proses yang sedang berjalan:
    ```bash
    ps -e
    ```

2. Menampilkan proses dalam format penuh:
    ```bash
    ps -f
    ```

3. Menampilkan proses yang dimiliki oleh pengguna tertentu:
    ```bash
    ps -u username
    ```

4. Menampilkan maklumat tentang proses dengan ID tertentu:
    ```bash
    ps -p 1234
    ```

5. Menampilkan semua proses dengan maklumat lengkap:
    ```bash
    ps aux
    ```

## Tips
- Gunakan `ps aux | grep [nama_proses]` untuk mencari proses tertentu dengan lebih mudah.
- Kombinasikan `ps` dengan perintah lain seperti `sort` untuk mengatur hasil mengikut penggunaan CPU atau memori.
- Untuk memantau proses secara berterusan, pertimbangkan untuk menggunakan perintah `top` atau `htop` sebagai alternatif.