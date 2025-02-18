# [Sistem Operasi] Debian Almquist Shell (dash) killall: [bunuh proses berdasarkan nama]

## Overview
Perintah `killall` digunakan untuk menghentikan semua proses yang berjalan dengan nama tertentu. Ini berguna untuk mengurus proses yang tidak responsif atau untuk mengurus sumber daya sistem dengan lebih baik.

## Usage
Berikut adalah sintaks asas untuk perintah `killall`:

```bash
killall [options] [arguments]
```

## Common Options
- `-s, --signal SIGNAL`: Menghantar isyarat tertentu kepada proses. Contohnya, `-s TERM` untuk menghentikan proses secara lembut.
- `-u, --user USER`: Hanya membunuh proses yang dimiliki oleh pengguna tertentu.
- `-v, --verbose`: Menunjukkan maklumat tambahan tentang proses yang dibunuh.
- `-i, --interactive`: Meminta pengesahan sebelum membunuh setiap proses.

## Common Examples
Berikut adalah beberapa contoh penggunaan `killall`:

1. **Membunuh semua proses dengan nama "firefox":**
   ```bash
   killall firefox
   ```

2. **Membunuh proses dengan isyarat tertentu (contohnya, SIGKILL):**
   ```bash
   killall -s KILL firefox
   ```

3. **Membunuh semua proses yang dimiliki oleh pengguna tertentu:**
   ```bash
   killall -u username
   ```

4. **Menggunakan pilihan verbose untuk melihat proses yang dibunuh:**
   ```bash
   killall -v firefox
   ```

5. **Meminta pengesahan sebelum membunuh proses:**
   ```bash
   killall -i firefox
   ```

## Tips
- Sentiasa semak nama proses dengan `ps aux` sebelum menggunakan `killall` untuk mengelakkan membunuh proses yang salah.
- Gunakan pilihan `-v` untuk mendapatkan maklumat tambahan, terutama jika anda membunuh banyak proses.
- Jika anda tidak pasti tentang proses yang ingin dibunuh, pertimbangkan untuk menggunakan `pkill` yang membenarkan pola pencarian yang lebih fleksibel.