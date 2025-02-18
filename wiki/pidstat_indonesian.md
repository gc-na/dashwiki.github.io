# [Sistem Operasi] Debian Almquist Shell (dash) pidstat Penggunaan: Memantau Statistik Proses

## Overview
Perintah `pidstat` digunakan untuk memantau statistik penggunaan sumber daya dari proses yang berjalan di sistem. Ini memberikan informasi tentang penggunaan CPU, memori, dan statistik lainnya berdasarkan ID proses (PID).

## Usage
Sintaks dasar dari perintah `pidstat` adalah sebagai berikut:

```bash
pidstat [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan `pidstat`:

- `-h`: Menampilkan header yang lebih jelas.
- `-r`: Menampilkan penggunaan memori.
- `-p <pid>`: Memantau proses tertentu berdasarkan ID proses.
- `-u`: Menampilkan penggunaan CPU.
- `-t`: Menampilkan statistik untuk semua thread dalam proses.

## Common Examples
Berikut adalah beberapa contoh penggunaan `pidstat`:

1. **Memantau penggunaan CPU untuk semua proses:**
   ```bash
   pidstat
   ```

2. **Memantau penggunaan CPU dan memori untuk proses tertentu:**
   ```bash
   pidstat -r -u -p 1234
   ```

3. **Menampilkan statistik untuk semua thread dalam proses:**
   ```bash
   pidstat -t -p 5678
   ```

4. **Menampilkan statistik dengan header yang lebih jelas:**
   ```bash
   pidstat -h
   ```

## Tips
- Gunakan opsi `-p` untuk fokus pada proses tertentu yang ingin Anda analisis.
- Kombinasikan opsi `-u` dan `-r` untuk mendapatkan gambaran lengkap tentang penggunaan CPU dan memori.
- Jalankan `pidstat` secara berkala dengan menggunakan `watch` untuk memantau perubahan dalam waktu nyata. Contoh:
  ```bash
  watch -n 1 pidstat -u
  ```