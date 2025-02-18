# [Sistem Operasi] Debian Almquist Shell (dash) pidstat: [memantau statistik proses]

## Overview
Perintah `pidstat` digunakan untuk memantau statistik penggunaan sumber daya oleh proses yang sedang berjalan di sistem. Ia memberikan informasi terperinci mengenai penggunaan CPU, memori, dan I/O untuk setiap proses, yang sangat berguna untuk analisis performa dan pengoptimuman sistem.

## Usage
Berikut adalah sintaks dasar untuk menggunakan perintah `pidstat`:

```bash
pidstat [options] [arguments]
```

## Common Options
- `-h`: Menampilkan bantuan dan informasi tentang penggunaan perintah.
- `-r`: Menampilkan statistik penggunaan memori.
- `-u`: Menampilkan statistik penggunaan CPU.
- `-p <pid>`: Memantau proses tertentu berdasarkan ID proses (PID).
- `-t`: Menampilkan statistik untuk semua thread dalam proses.

## Common Examples
Berikut adalah beberapa contoh penggunaan `pidstat`:

1. **Memantau penggunaan CPU semua proses:**
   ```bash
   pidstat
   ```

2. **Memantau penggunaan memori untuk proses tertentu:**
   ```bash
   pidstat -r -p 1234
   ```

3. **Menampilkan statistik penggunaan CPU setiap 2 detik:**
   ```bash
   pidstat -u 2
   ```

4. **Menampilkan statistik untuk semua thread dalam proses tertentu:**
   ```bash
   pidstat -t -p 5678
   ```

## Tips
- Gunakan opsi `-h` untuk mendapatkan bantuan dan informasi lebih lanjut tentang penggunaan perintah.
- Pertimbangkan untuk menggunakan `pidstat` bersama dengan perintah lain seperti `grep` untuk menyaring hasil berdasarkan kriteria tertentu.
- Untuk analisis yang lebih mendalam, simpan output `pidstat` ke dalam fail log untuk analisis selanjutnya.