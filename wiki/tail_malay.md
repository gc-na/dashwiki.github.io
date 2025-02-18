# [Sistem Operasi] Debian Almquist Shell (dash) tail Penggunaan: Menunjukkan akhir fail

## Overview
Perintah `tail` digunakan untuk memaparkan baris terakhir dari satu atau lebih fail. Ia sangat berguna untuk melihat log fail atau output yang sedang dihasilkan oleh proses lain.

## Usage
Sintaks asas bagi perintah `tail` adalah seperti berikut:

```
tail [options] [arguments]
```

## Common Options
- `-n [number]`: Menentukan jumlah baris terakhir yang ingin dipaparkan. Contohnya, `-n 10` untuk memaparkan 10 baris terakhir.
- `-f`: Mengikuti fail secara langsung, memaparkan baris baru yang ditambah ke fail tersebut secara real-time.
- `-c [number]`: Menentukan jumlah bait terakhir yang ingin dipaparkan.

## Common Examples
Berikut adalah beberapa contoh penggunaan `tail`:

1. Memaparkan 10 baris terakhir dari fail `logfile.txt`:
   ```sh
   tail logfile.txt
   ```

2. Memaparkan 20 baris terakhir dari fail `logfile.txt`:
   ```sh
   tail -n 20 logfile.txt
   ```

3. Mengikuti fail `logfile.txt` secara langsung:
   ```sh
   tail -f logfile.txt
   ```

4. Memaparkan 50 bait terakhir dari fail `logfile.txt`:
   ```sh
   tail -c 50 logfile.txt
   ```

## Tips
- Gunakan `tail -f` untuk memantau log secara langsung semasa aplikasi sedang berjalan.
- Gabungkan `tail` dengan perintah lain menggunakan pipe (`|`) untuk analisis data yang lebih lanjut.
- Jika anda ingin menghentikan pemantauan fail dengan `tail -f`, tekan `Ctrl + C`.