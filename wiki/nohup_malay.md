# [Sistem Operasi] Debian Almquist Shell (dash) nohup: Menjalankan proses tanpa gangguan

## Overview
Perintah `nohup` digunakan untuk menjalankan proses di latar belakang tanpa terpengaruh oleh sesi terminal yang sedang aktif. Ini berguna untuk memastikan bahawa proses tetap berjalan walaupun sesi terminal ditutup.

## Usage
Berikut adalah sintaks asas untuk perintah `nohup`:

```bash
nohup [options] [arguments]
```

## Common Options
- `&`: Menjalankan proses di latar belakang.
- `-h`: Menunjukkan bantuan untuk perintah nohup.
- `-p`: Menjalankan nohup dalam konteks proses yang ada.

## Common Examples
Berikut adalah beberapa contoh penggunaan `nohup`:

1. Menjalankan skrip shell di latar belakang:
   ```bash
   nohup ./myscript.sh &
   ```

2. Menjalankan perintah `ping` dan menyimpan output ke dalam fail:
   ```bash
   nohup ping google.com > ping_output.txt &
   ```

3. Menjalankan aplikasi Java tanpa gangguan:
   ```bash
   nohup java -jar myapp.jar &
   ```

## Tips
- Selalu gunakan `&` di akhir perintah untuk memastikan proses berjalan di latar belakang.
- Periksa fail `nohup.out` untuk melihat output dari proses yang dijalankan dengan `nohup`.
- Gunakan perintah `jobs` untuk melihat proses latar belakang yang sedang berjalan.