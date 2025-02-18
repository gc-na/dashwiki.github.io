# [Sistem Operasi] Debian Almquist Shell (dash) at: Menjadwalkan tugas untuk dijalankan di masa depan

## Overview
Perintah `at` digunakan untuk menjadwalkan tugas agar dijalankan pada waktu tertentu di masa depan. Ini berguna untuk mengotomatiskan tugas yang perlu dilakukan sekali, tanpa harus menunggu secara manual.

## Usage
Sintaks dasar dari perintah `at` adalah sebagai berikut:

```
at [options] [arguments]
```

## Common Options
- `-f FILE`: Membaca perintah dari file yang ditentukan.
- `-m`: Mengirim email kepada pengguna setelah perintah selesai dijalankan.
- `-q QUEUE`: Menentukan antrean untuk menjalankan tugas.
- `-t TIME`: Menentukan waktu dalam format tertentu (misalnya, `YYMMDDhhmm`).

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `at`:

1. Menjadwalkan perintah untuk dijalankan pada waktu tertentu:
   ```bash
   echo "backup.sh" | at 02:00
   ```

2. Menjadwalkan perintah untuk dijalankan pada hari tertentu:
   ```bash
   echo "echo 'Hello, World!'" | at 5pm tomorrow
   ```

3. Menjalankan skrip dari file:
   ```bash
   at -f /path/to/script.sh 3:00
   ```

4. Menjadwalkan perintah dan mengirim email setelah selesai:
   ```bash
   echo "run_report.sh" | at -m 10:00
   ```

## Tips
- Pastikan untuk memeriksa apakah layanan `atd` berjalan di sistem Anda agar perintah `at` dapat berfungsi dengan baik.
- Gunakan `atq` untuk melihat daftar tugas yang telah dijadwalkan.
- Gunakan `atrm JOB_ID` untuk menghapus tugas yang telah dijadwalkan jika Anda berubah pikiran.