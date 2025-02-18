# [Sistem Operasi] Debian Almquist Shell (dash) hostname penggunaan: [menetapkan nama host]

## Overview
Perintah `hostname` digunakan untuk menampilkan atau menetapkan nama host sistem. Nama host adalah nama unik yang digunakan untuk mengenali komputer dalam rangkaian. Dengan menggunakan perintah ini, pengguna dapat mengetahui nama host semasa atau mengubahnya jika diperlukan.

## Usage
Berikut adalah sintaks asas untuk perintah `hostname`:

```bash
hostname [options] [arguments]
```

## Common Options
- `-f`, `--fqdn`: Menampilkan nama host sepenuhnya (Fully Qualified Domain Name).
- `-i`, `--ip-address`: Menampilkan alamat IP untuk nama host yang diberikan.
- `-s`, `--short`: Menampilkan nama host pendek tanpa domain.
- `-V`, `--version`: Menampilkan versi perintah `hostname`.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan perintah `hostname`:

1. **Menampilkan nama host semasa:**
   ```bash
   hostname
   ```

2. **Menampilkan nama host sepenuhnya:**
   ```bash
   hostname -f
   ```

3. **Menampilkan alamat IP untuk nama host:**
   ```bash
   hostname -i
   ```

4. **Menetapkan nama host baru:**
   ```bash
   hostname new-hostname
   ```

5. **Menampilkan nama host pendek:**
   ```bash
   hostname -s
   ```

## Tips
- Pastikan untuk menjalankan perintah `hostname` dengan hak akses yang sesuai jika anda ingin menetapkan nama host baru.
- Setelah mengubah nama host, anda mungkin perlu mengedit fail `/etc/hosts` untuk memastikan bahawa nama host baru dikenali dengan betul dalam sistem.
- Gunakan perintah `hostname -V` untuk memeriksa versi perintah `hostname` yang sedang digunakan, terutama jika anda menghadapi masalah.