# [Sistem Operasi] Debian Almquist Shell (dash) basename Penggunaan: Mengambil nama file dari path

## Overview
Perintah `basename` digunakan untuk mengambil nama file dari path lengkap. Ini berguna ketika Anda hanya ingin mengekstrak nama file tanpa bagian direktori.

## Usage
Berikut adalah sintaks dasar dari perintah `basename`:

```bash
basename [options] [arguments]
```

## Common Options
- `-a`: Mengambil semua nama file dari daftar argumen.
- `-s`: Menghapus suffix tertentu dari nama file.
- `--help`: Menampilkan bantuan penggunaan perintah.

## Common Examples
Berikut adalah beberapa contoh penggunaan `basename`:

1. Mengambil nama file dari path lengkap:
   ```bash
   basename /home/user/file.txt
   ```
   Output:
   ```
   file.txt
   ```

2. Menghapus suffix dari nama file:
   ```bash
   basename /home/user/file.txt .txt
   ```
   Output:
   ```
   file
   ```

3. Mengambil nama file dari beberapa path:
   ```bash
   basename -a /home/user/file1.txt /home/user/file2.txt
   ```
   Output:
   ```
   file1.txt
   file2.txt
   ```

## Tips
- Gunakan opsi `-s` untuk menghapus ekstensi file yang tidak diinginkan saat hanya ingin mendapatkan nama dasar.
- Perintah ini sangat berguna dalam skrip shell untuk memproses daftar file.
- Ingat bahwa `basename` hanya mengembalikan nama file terakhir dari path yang diberikan.