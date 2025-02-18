# [Sistem Operasi] Debian Almquist Shell (dash) netstat Penggunaan: Memaparkan statistik rangkaian

## Overview
Perintah `netstat` digunakan untuk memaparkan statistik rangkaian dan maklumat tentang sambungan rangkaian yang aktif, termasuk alamat IP, port, dan status sambungan. Ia berguna untuk mendiagnosis masalah rangkaian dan memantau aktiviti rangkaian pada sistem.

## Usage
Berikut adalah sintaks asas untuk perintah `netstat`:

```
netstat [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa untuk `netstat` beserta penjelasan ringkas:

- `-a`: Memaparkan semua sambungan dan port yang mendengar.
- `-t`: Menunjukkan sambungan TCP sahaja.
- `-u`: Menunjukkan sambungan UDP sahaja.
- `-n`: Memaparkan alamat IP dan nombor port dalam format numerik.
- `-l`: Menunjukkan hanya port yang sedang mendengar.

## Common Examples
Berikut adalah beberapa contoh praktikal menggunakan `netstat`:

1. **Memaparkan semua sambungan dan port yang mendengar:**
   ```bash
   netstat -a
   ```

2. **Menunjukkan sambungan TCP sahaja:**
   ```bash
   netstat -t
   ```

3. **Menunjukkan sambungan UDP sahaja:**
   ```bash
   netstat -u
   ```

4. **Memaparkan sambungan dengan alamat IP dan nombor port dalam format numerik:**
   ```bash
   netstat -n
   ```

5. **Menunjukkan hanya port yang sedang mendengar:**
   ```bash
   netstat -l
   ```

## Tips
- Gunakan pilihan `-p` untuk melihat proses yang berkaitan dengan sambungan rangkaian.
- Gabungkan beberapa pilihan untuk mendapatkan maklumat yang lebih terperinci, contohnya `netstat -tuln`.
- Jalankan `netstat` dengan hak akses root untuk mendapatkan maklumat yang lebih lengkap tentang sambungan yang sedang aktif.