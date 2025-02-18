# [Sistem Operasi] Debian Almquist Shell (dash) ping6: [menghantar paket ICMPv6]

## Overview
Perintah `ping6` digunakan untuk menguji sambungan rangkaian dengan menghantar paket ICMPv6 ke alamat IPv6 tertentu. Ia membantu dalam menentukan sama ada host tertentu dapat dihubungi melalui rangkaian dan mengukur masa yang diambil untuk menerima balasan.

## Usage
Sintaks asas untuk perintah `ping6` adalah seperti berikut:
```
ping6 [options] [arguments]
```

## Common Options
- `-c <count>`: Menentukan jumlah paket yang akan dihantar.
- `-i <interval>`: Menetapkan selang masa antara setiap paket yang dihantar.
- `-w <deadline>`: Menentukan waktu maksimum untuk menghantar paket.
- `-s <size>`: Menentukan saiz paket yang akan dihantar.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `ping6`:

1. Menghantar paket ke alamat IPv6 tertentu:
   ```bash
   ping6 2001:db8::1
   ```

2. Menghantar 5 paket ke alamat IPv6:
   ```bash
   ping6 -c 5 2001:db8::1
   ```

3. Menghantar paket dengan saiz 128 byte:
   ```bash
   ping6 -s 128 2001:db8::1
   ```

4. Menghantar paket dengan selang 2 detik antara setiap paket:
   ```bash
   ping6 -i 2 2001:db8::1
   ```

5. Menghantar paket sehingga 10 saat:
   ```bash
   ping6 -w 10 2001:db8::1
   ```

## Tips
- Gunakan opsi `-c` untuk mengelakkan pengiriman paket yang tidak terhad, terutama jika anda hanya ingin melakukan ujian ringkas.
- Perhatikan waktu balasan yang ditunjukkan; ini dapat memberikan petunjuk tentang keadaan rangkaian.
- Jika anda tidak menerima balasan, pastikan bahawa alamat IPv6 yang digunakan adalah betul dan host tersebut aktif dalam rangkaian.