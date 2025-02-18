# [Sistem Operasi] Debian Almquist Shell (dash) at: Menjadwalkan Tugas

## Overview
Perintah `at` digunakan untuk menjadwalkan tugas yang akan dijalankan pada waktu tertentu di masa depan. Ini berguna untuk menjalankan skrip atau perintah tanpa perlu menunggu di terminal.

## Usage
Sintaks dasar untuk perintah `at` adalah seperti berikut:

```
at [options] [arguments]
```

## Common Options
- `-f FILE`: Mengambil perintah dari fail yang ditentukan.
- `-m`: Menghantar e-mel kepada pengguna setelah tugas selesai.
- `-q QUEUE`: Menentukan antrian untuk tugas yang dijadwalkan.
- `-l`: Menyenaraikan semua tugas yang telah dijadwalkan.
- `-d JOB_ID`: Menghapus tugas yang dijadwalkan berdasarkan ID tugas.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan perintah `at`:

1. Menjadwalkan perintah untuk dijalankan pada waktu tertentu:
   ```bash
   echo "echo Hello, World!" | at 10:00
   ```

2. Menjadwalkan skrip untuk dijalankan pada hari berikutnya:
   ```bash
   at now + 1 day < myscript.sh
   ```

3. Menggunakan fail untuk menjadwalkan perintah:
   ```bash
   at -f mycommands.txt 15:00
   ```

4. Menyenaraikan semua tugas yang telah dijadwalkan:
   ```bash
   at -l
   ```

5. Menghapus tugas yang dijadwalkan:
   ```bash
   at -d 2
   ```

## Tips
- Pastikan untuk memeriksa waktu sistem anda sebelum menjadwalkan tugas.
- Gunakan opsi `-m` untuk mendapatkan pemberitahuan melalui e-mel setelah tugas selesai.
- Sentiasa semak senarai tugas yang dijadwalkan dengan `at -l` untuk mengelakkan konflik.