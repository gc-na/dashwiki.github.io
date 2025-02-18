# [Sistem Operasi] Debian Almquist Shell (dash) strace Penggunaan: Mengesan sistem panggilan

## Overview
Perintah `strace` digunakan untuk mengesan dan mendiagnosis sistem panggilan dan isyarat yang dilakukan oleh proses dalam sistem Linux. Ia sangat berguna untuk pemaju dan pentadbir sistem untuk memahami bagaimana aplikasi berinteraksi dengan kernel dan sumber sistem.

## Usage
Sintaks asas bagi perintah `strace` adalah seperti berikut:

```bash
strace [options] [arguments]
```

## Common Options
- `-c`: Mengira statistik sistem panggilan.
- `-e <expression>`: Menetapkan penapis untuk sistem panggilan yang ingin dikesan.
- `-o <file>`: Mengarahkan output ke dalam fail yang ditentukan.
- `-p <pid>`: Mengesan proses yang sedang berjalan dengan ID proses tertentu.
- `-f`: Mengesan proses kanak-kanak yang dicipta oleh proses induk.

## Common Examples
Berikut adalah beberapa contoh penggunaan `strace`:

1. Mengesan semua sistem panggilan untuk perintah `ls`:
   ```bash
   strace ls
   ```

2. Mengarahkan output ke dalam fail `output.txt`:
   ```bash
   strace -o output.txt ls
   ```

3. Mengira statistik sistem panggilan untuk perintah `cat`:
   ```bash
   strace -c cat file.txt
   ```

4. Mengesan proses yang sedang berjalan dengan ID proses 1234:
   ```bash
   strace -p 1234
   ```

5. Menggunakan penapis untuk hanya mengesan sistem panggilan `open` dan `close`:
   ```bash
   strace -e trace=open,close ls
   ```

## Tips
- Gunakan `-o` untuk menyimpan output ke dalam fail jika anda ingin menganalisisnya kemudian.
- Untuk mengelakkan output yang terlalu panjang, gunakan `-c` untuk mendapatkan ringkasan statistik.
- Pastikan anda mempunyai keizinan yang diperlukan untuk mengesan proses lain, terutamanya jika ia bukan milik anda.