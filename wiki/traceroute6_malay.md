# [Sistem Operasi] Debian Almquist Shell (dash) traceroute6 Penggunaan: Menjejak laluan IPv6

## Overview
Perintah `traceroute6` digunakan untuk menjejak laluan yang dilalui oleh paket data dalam rangkaian IPv6. Ia membantu pengguna memahami bagaimana data bergerak dari satu titik ke titik lain dalam rangkaian, serta mengenal pasti sebarang masalah yang mungkin timbul sepanjang laluan tersebut.

## Usage
Sintaks asas untuk menggunakan perintah `traceroute6` adalah seperti berikut:

```
traceroute6 [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa yang boleh digunakan dengan `traceroute6`:

- `-m <max_ttl>`: Menetapkan nilai maksimum Time To Live (TTL) untuk paket.
- `-p <port>`: Menentukan port yang akan digunakan untuk sambungan.
- `-n`: Mengelakkan resolusi nama host, hanya menunjukkan alamat IP.
- `-q <nqueries>`: Menetapkan bilangan pertanyaan yang dihantar untuk setiap hop.
- `-w <timeout>`: Menetapkan masa tamat untuk setiap pertanyaan.

## Common Examples
Berikut adalah beberapa contoh penggunaan `traceroute6`:

1. Menjejak laluan ke alamat IPv6 tertentu:
   ```bash
   traceroute6 2001:db8::1
   ```

2. Menetapkan nilai maksimum TTL kepada 30:
   ```bash
   traceroute6 -m 30 2001:db8::1
   ```

3. Menggunakan port tertentu (contohnya, port 80):
   ```bash
   traceroute6 -p 80 2001:db8::1
   ```

4. Mengelakkan resolusi nama host:
   ```bash
   traceroute6 -n 2001:db8::1
   ```

5. Menghantar 5 pertanyaan untuk setiap hop:
   ```bash
   traceroute6 -q 5 2001:db8::1
   ```

## Tips
- Sentiasa gunakan pilihan `-n` jika anda ingin mempercepatkan proses, terutama dalam rangkaian yang mempunyai banyak hop.
- Periksa sambungan rangkaian anda sebelum menggunakan `traceroute6` untuk memastikan bahawa anda dapat mengakses alamat IPv6 yang ingin dijejaki.
- Gunakan pilihan `-m` untuk mengelakkan masa tamat yang terlalu lama jika anda tahu laluan yang ingin dijejaki tidak terlalu panjang.