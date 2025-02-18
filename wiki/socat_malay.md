# [Sistem Operasi] Debian Almquist Shell (dash) socat: [menghubungkan aliran data]

## Overview
Perintah `socat` adalah alat yang digunakan untuk menghubungkan dua aliran data, seperti soket, fail, atau peranti. Ia membolehkan pengguna untuk mengalirkan data antara sumber yang berbeza, menjadikannya berguna untuk pelbagai aplikasi seperti pemantauan rangkaian, pengujian, dan pengendalian data.

## Usage
Berikut adalah sintaks asas untuk perintah `socat`:

```bash
socat [options] [arguments]
```

## Common Options
- `-d`: Mengaktifkan mod debug, memberikan maklumat tambahan tentang operasi.
- `-v`: Mengaktifkan mod verbose, menunjukkan lebih banyak maklumat tentang data yang dipindahkan.
- `-u`: Menetapkan aliran sebagai tidak terputus (unidirectional).
- `-b <size>`: Menetapkan saiz buffer untuk pemindahan data.

## Common Examples
Berikut adalah beberapa contoh penggunaan `socat`:

1. **Menghubungkan dua soket TCP:**
   ```bash
   socat TCP-LISTEN:1234,fork TCP:example.com:80
   ```
   Contoh ini mendengar pada port 1234 dan meneruskan sambungan ke `example.com` pada port 80.

2. **Menghantar data dari fail ke soket:**
   ```bash
   socat -u FILE:/path/to/file TCP:example.com:1234
   ```
   Dalam contoh ini, data dari fail dihantar ke soket TCP pada `example.com` di port 1234.

3. **Membaca dari stdin dan menghantar ke soket:**
   ```bash
   socat -u - TCP:localhost:8080
   ```
   Perintah ini membolehkan pengguna memasukkan data melalui stdin dan menghantarnya ke soket TCP di localhost pada port 8080.

4. **Menghubungkan dua peranti:**
   ```bash
   socat /dev/ttyUSB0 /dev/ttyUSB1
   ```
   Ini menghubungkan dua peranti USB secara langsung, membolehkan data mengalir antara mereka.

## Tips
- Sentiasa gunakan pilihan `-d` atau `-v` semasa pengujian untuk mendapatkan maklumat tambahan tentang apa yang berlaku.
- Pastikan untuk memeriksa hak akses fail dan peranti yang digunakan untuk mengelakkan masalah sambungan.
- Gunakan `socat` dalam skrip untuk automasi tugas yang melibatkan pemindahan data antara pelbagai sumber.