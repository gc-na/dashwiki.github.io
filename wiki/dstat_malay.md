# [Sistem Operasi] Debian Almquist Shell (dash) dstat Penggunaan: Memantau sumber sistem secara langsung

## Overview
Perintah `dstat` adalah alat yang berguna untuk memantau sumber sistem secara langsung. Ia menggabungkan beberapa alat pemantauan sistem yang berbeza dan memberikan maklumat tentang penggunaan CPU, memori, disk, dan rangkaian dalam satu paparan yang mudah dibaca.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `dstat`:

```
dstat [options] [arguments]
```

## Common Options
Beberapa pilihan umum untuk `dstat` termasuk:

- `-c` : Paparkan penggunaan CPU.
- `-d` : Paparkan statistik disk.
- `-n` : Paparkan statistik rangkaian.
- `-m` : Paparkan penggunaan memori.
- `--help` : Tunjukkan bantuan dan pilihan yang tersedia.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `dstat`:

1. **Paparkan penggunaan CPU dan memori:**
   ```bash
   dstat -c -m
   ```

2. **Paparkan statistik disk dan rangkaian:**
   ```bash
   dstat -d -n
   ```

3. **Paparkan semua sumber sistem secara serentak:**
   ```bash
   dstat
   ```

4. **Simpan output ke dalam fail untuk analisis lanjut:**
   ```bash
   dstat > output.txt
   ```

## Tips
- Gunakan pilihan `-t` untuk menambah cap waktu pada output, membantu dalam analisis data.
- Jalankan `dstat` dengan pilihan `--full` untuk mendapatkan maklumat yang lebih terperinci.
- Pertimbangkan untuk menggunakan `dstat` dalam skrip pemantauan untuk memudahkan pengawasan sumber sistem secara automatik.