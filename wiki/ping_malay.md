# [Sistem Operasi] Debian Almquist Shell (dash) ping penggunaan: Menguji sambungan rangkaian

## Overview
Perintah `ping` digunakan untuk menguji sambungan rangkaian antara komputer anda dan host lain. Ia menghantar paket ICMP Echo Request ke alamat IP yang ditentukan dan menunggu balasan. Ini berguna untuk menentukan sama ada host tersebut dapat diakses dan untuk mengukur masa yang diambil untuk menghantar dan menerima data.

## Usage
Berikut adalah sintaks asas untuk perintah `ping`:

```
ping [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa untuk perintah `ping`:

- `-c [count]`: Menentukan jumlah paket yang akan dihantar.
- `-i [interval]`: Menetapkan selang waktu antara paket yang dihantar.
- `-s [size]`: Menentukan saiz paket yang dihantar.
- `-t [ttl]`: Menetapkan nilai Time To Live untuk paket.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `ping`:

1. Menghantar paket ke alamat IP tertentu:
   ```bash
   ping 8.8.8.8
   ```

2. Menghantar 5 paket ke alamat domain:
   ```bash
   ping -c 5 google.com
   ```

3. Menghantar paket dengan saiz tertentu:
   ```bash
   ping -s 100 192.168.1.1
   ```

4. Menghantar paket dengan selang waktu 2 saat:
   ```bash
   ping -i 2 example.com
   ```

## Tips
- Gunakan pilihan `-c` untuk menghentikan ping secara automatik setelah jumlah paket tertentu dihantar.
- Jika anda ingin menghentikan ping yang sedang berjalan, tekan `Ctrl + C`.
- Periksa sambungan rangkaian dengan ping ke alamat IP yang diketahui, seperti 8.8.8.8, untuk memastikan sambungan internet berfungsi.