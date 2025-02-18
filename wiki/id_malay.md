# [Debian] Debian Almquist Shell (dash) id: [menunjukkan maklumat pengguna]

## Overview
Perintah `id` dalam shell Debian Almquist (dash) digunakan untuk memaparkan maklumat mengenai pengguna semasa atau pengguna lain. Ia memberikan maklumat seperti UID (User ID), GID (Group ID), dan kumpulan yang dimiliki oleh pengguna.

## Usage
Berikut adalah sintaks asas untuk perintah `id`:

```
id [options] [arguments]
```

## Common Options
- `-u`: Menunjukkan UID pengguna.
- `-g`: Menunjukkan GID kumpulan utama pengguna.
- `-G`: Menunjukkan semua GID yang dimiliki oleh pengguna.
- `-n`: Menunjukkan nama pengguna atau nama kumpulan daripada ID.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `id`:

1. **Menunjukkan maklumat pengguna semasa:**
   ```bash
   id
   ```

2. **Menunjukkan UID pengguna semasa:**
   ```bash
   id -u
   ```

3. **Menunjukkan GID kumpulan utama pengguna:**
   ```bash
   id -g
   ```

4. **Menunjukkan semua GID yang dimiliki oleh pengguna:**
   ```bash
   id -G
   ```

5. **Menunjukkan maklumat pengguna lain (contohnya, pengguna 'john'):**
   ```bash
   id john
   ```

## Tips
- Gunakan `id` tanpa sebarang pilihan untuk mendapatkan maklumat lengkap tentang pengguna semasa.
- Untuk memeriksa maklumat pengguna lain, pastikan anda mempunyai keizinan yang sesuai.
- Perintah ini berguna untuk skrip dan pengurusan sistem untuk mengesahkan identiti pengguna dan kumpulan.