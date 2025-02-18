# [Sistem Operasi] Debian Almquist Shell (dash) ulimit: Mengawal had sumber sistem

## Overview
Perintah `ulimit` digunakan untuk mengawal dan menetapkan had sumber sistem yang boleh digunakan oleh proses dalam shell. Ini termasuk had untuk memori, jumlah fail yang boleh dibuka, dan banyak lagi. Dengan menggunakan `ulimit`, pengguna boleh melindungi sistem daripada penggunaan sumber yang berlebihan oleh proses tertentu.

## Usage
Sintaks asas untuk perintah `ulimit` adalah seperti berikut:

```bash
ulimit [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa untuk `ulimit` beserta penjelasan ringkas:

- `-a`: Menunjukkan semua had sumber yang sedang ditetapkan.
- `-c`: Menetapkan had saiz fail core.
- `-d`: Menetapkan had saiz segmen data.
- `-f`: Menetapkan had saiz fail maksimum.
- `-l`: Menetapkan had saiz memori yang boleh dikunci.
- `-n`: Menetapkan had bilangan fail yang boleh dibuka.
- `-s`: Menetapkan had saiz stack.
- `-t`: Menetapkan had masa CPU maksimum.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `ulimit`:

1. **Menunjukkan semua had sumber:**
   ```bash
   ulimit -a
   ```

2. **Menetapkan had maksimum saiz fail kepada 100MB:**
   ```bash
   ulimit -f 102400
   ```

3. **Menetapkan had bilangan fail yang boleh dibuka kepada 200:**
   ```bash
   ulimit -n 200
   ```

4. **Menetapkan had saiz stack kepada 8MB:**
   ```bash
   ulimit -s 8192
   ```

5. **Menetapkan had masa CPU maksimum kepada 60 saat:**
   ```bash
   ulimit -t 60
   ```

## Tips
- Sentiasa semak had sumber semasa sebelum menjalankan aplikasi yang memerlukan sumber tinggi.
- Gunakan `ulimit -a` untuk mendapatkan gambaran keseluruhan tentang semua had yang ditetapkan.
- Pastikan untuk menetapkan had yang sesuai untuk aplikasi tertentu untuk mengelakkan masalah prestasi atau keruntuhan sistem.