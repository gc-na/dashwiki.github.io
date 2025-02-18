# [Sistem Operasi] Debian Almquist Shell (dash) traceroute penggunaan: Menjejak laluan rangkaian

## Overview
Perintah `traceroute` digunakan untuk menjejak laluan yang diambil oleh paket data dari komputer anda ke alamat IP atau nama host tertentu. Ia membantu dalam mendiagnosis masalah rangkaian dengan menunjukkan setiap hop (peranti) yang dilalui oleh paket.

## Usage
Sintaks asas untuk perintah `traceroute` adalah seperti berikut:

```bash
traceroute [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan umum untuk `traceroute` beserta penjelasan ringkas:

- `-m <max_ttl>`: Menetapkan nilai maksimum Time To Live (TTL) untuk paket.
- `-n`: Menggunakan alamat IP tanpa melakukan pengesanan nama host.
- `-p <port>`: Menetapkan port yang akan digunakan untuk pengesanan.
- `-q <nqueries>`: Menetapkan bilangan paket yang dihantar pada setiap hop.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `traceroute`:

1. Menjejak laluan ke alamat IP:
    ```bash
    traceroute 8.8.8.8
    ```

2. Menjejak laluan ke nama host:
    ```bash
    traceroute www.google.com
    ```

3. Menjejak laluan tanpa pengesanan nama host:
    ```bash
    traceroute -n 8.8.8.8
    ```

4. Menetapkan nilai maksimum TTL:
    ```bash
    traceroute -m 10 www.example.com
    ```

## Tips
- Gunakan pilihan `-n` untuk mempercepatkan proses jika anda tidak memerlukan nama host.
- Jika anda menghadapi masalah dengan firewall, cuba gunakan pilihan `-p` untuk menyesuaikan port yang digunakan.
- Perhatikan hasil traceroute untuk mengenal pasti di mana masalah rangkaian mungkin berlaku, seperti hop yang mempunyai masa respons yang tinggi.