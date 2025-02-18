# [Sistem Operasi] Debian Almquist Shell (dash) dirname Penggunaan: Mengambil nama direktori dari jalur fail

## Overview
Perintah `dirname` digunakan untuk mengambil nama direktori dari jalur fail yang diberikan. Ia mengembalikan bahagian jalur yang menunjukkan lokasi direktori, tanpa nama fail itu sendiri.

## Usage
Berikut adalah sintaks asas untuk perintah `dirname`:

```
dirname [options] [arguments]
```

## Common Options
- `-z`, `--zero`: Menggunakan pemisah null untuk output.
- `--help`: Menunjukkan bantuan untuk perintah ini.
- `--version`: Menunjukkan versi perintah `dirname`.

## Common Examples
Berikut adalah beberapa contoh penggunaan `dirname`:

1. Mengambil nama direktori dari jalur penuh:
   ```sh
   dirname /home/user/documents/file.txt
   ```
   Output:
   ```
   /home/user/documents
   ```

2. Mengambil nama direktori dari jalur relatif:
   ```sh
   dirname ./projects/code/main.py
   ```
   Output:
   ```
   ./projects/code
   ```

3. Menggunakan `dirname` dengan beberapa jalur:
   ```sh
   dirname /var/log/syslog /usr/bin/python3
   ```
   Output:
   ```
   /var/log
   /usr/bin
   ```

4. Menggunakan `dirname` dengan pemisah null:
   ```sh
   dirname -z /home/user/file1.txt\0/home/user/file2.txt
   ```
   Output:
   ```
   /home/user
   /home/user
   ```

## Tips
- Gunakan `dirname` dalam skrip shell untuk memudahkan pengendalian jalur fail.
- Gabungkan `dirname` dengan perintah lain seperti `basename` untuk manipulasi jalur yang lebih kompleks.
- Sentiasa semak jalur yang anda berikan untuk memastikan ia wujud bagi mengelakkan kesilapan.