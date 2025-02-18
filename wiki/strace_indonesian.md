# [Indonesian] Debian Almquist Shell (dash) strace: Melacak sistem panggilan

## Overview
Perintah `strace` digunakan untuk melacak dan mendiagnosis sistem panggilan yang dilakukan oleh program. Ini sangat berguna untuk memahami bagaimana program berinteraksi dengan kernel dan sumber daya sistem lainnya.

## Usage
Berikut adalah sintaks dasar dari perintah `strace`:

```bash
strace [options] [arguments]
```

## Common Options
- `-c`: Menghitung statistik sistem panggilan dan menampilkan ringkasan.
- `-f`: Mengikuti proses anak yang dibuat dengan `fork`.
- `-e trace=<event>`: Menentukan jenis peristiwa yang ingin dilacak, seperti `file`, `network`, dll.
- `-o <file>`: Mengalihkan output ke file yang ditentukan.

## Common Examples
Berikut adalah beberapa contoh penggunaan `strace`:

1. Melacak sistem panggilan dari sebuah program:
   ```bash
   strace ls
   ```

2. Menghitung statistik sistem panggilan:
   ```bash
   strace -c ls
   ```

3. Mengikuti proses anak:
   ```bash
   strace -f bash -c 'echo hello; sleep 1;'
   ```

4. Menyimpan output ke dalam file:
   ```bash
   strace -o output.txt ls
   ```

5. Melacak hanya sistem panggilan file:
   ```bash
   strace -e trace=file ls
   ```

## Tips
- Gunakan opsi `-c` untuk mendapatkan ringkasan cepat dari sistem panggilan yang paling sering digunakan.
- Jika Anda melacak program yang menghasilkan banyak output, pertimbangkan untuk mengalihkan output ke file untuk analisis lebih lanjut.
- Menggunakan opsi `-f` sangat berguna saat bekerja dengan program yang membuat proses anak, agar Anda dapat melihat semua interaksi.