# [Sistem Operasi] Debian Almquist Shell (dash) iotop: Memantau penggunaan I/O

## Overview
Perintah `iotop` digunakan untuk memantau penggunaan input/output (I/O) pada sistem Linux. Ia memberikan gambaran tentang proses yang menggunakan I/O disk, membolehkan pengguna untuk mengenal pasti aplikasi yang mungkin menyebabkan masalah prestasi.

## Usage
Sintaks asas untuk menggunakan `iotop` adalah seperti berikut:

```
iotop [options] [arguments]
```

## Common Options
- `-o`, `--only`: Hanya tunjukkan proses yang sedang menggunakan I/O.
- `-b`, `--batch`: Jalankan dalam mod batch, sesuai untuk output ke fail.
- `-n NUM`, `--iter NUM`: Tentukan berapa kali untuk mengulangi pemantauan.
- `-d SEC`, `--delay SEC`: Tentukan selang masa dalam saat antara kemas kini.

## Common Examples
Berikut adalah beberapa contoh penggunaan `iotop`:

1. **Menjalankan iotop untuk melihat semua proses:**
   ```bash
   iotop
   ```

2. **Menunjukkan hanya proses yang menggunakan I/O:**
   ```bash
   iotop -o
   ```

3. **Menjalankan iotop dalam mod batch selama 10 iterasi:**
   ```bash
   iotop -b -n 10
   ```

4. **Menetapkan selang masa 2 saat antara kemas kini:**
   ```bash
   iotop -d 2
   ```

## Tips
- Gunakan `iotop` dengan hak akses root untuk mendapatkan maklumat yang lebih lengkap tentang semua proses.
- Jika anda menggunakan mod batch, pertimbangkan untuk mengalihkan output ke fail untuk analisis lebih lanjut.
- Perhatikan proses yang menggunakan I/O secara berlebihan, kerana ini mungkin menunjukkan masalah yang perlu ditangani.