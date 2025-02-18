# [Sistem Operasi] Debian Almquist Shell (dash) basename: [menyediakan nama fail tanpa laluan]

## Overview
Perintah `basename` digunakan untuk mengeluarkan nama fail dari laluan penuh. Ia berguna untuk mendapatkan nama fail sahaja tanpa direktori yang mendahuluinya.

## Usage
Sintaks asas untuk perintah `basename` adalah seperti berikut:

```
basename [options] [arguments]
```

## Common Options
- `-a`: Mengambil semua nama fail yang diberikan dan mengeluarkan nama fail tanpa laluan untuk setiap satu.
- `-s`: Mengeluarkan nama fail tanpa sambungan tertentu yang ditentukan.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `basename`:

1. Mengeluarkan nama fail dari laluan penuh:
   ```sh
   basename /usr/local/bin/script.sh
   ```
   Output:
   ```
   script.sh
   ```

2. Mengeluarkan nama fail tanpa sambungan:
   ```sh
   basename /usr/local/bin/script.sh .sh
   ```
   Output:
   ```
   script
   ```

3. Menggunakan pilihan `-a` untuk mengeluarkan nama fail dari beberapa laluan:
   ```sh
   basename -a /usr/local/bin/script.sh /home/user/document.txt
   ```
   Output:
   ```
   script.sh
   document.txt
   ```

## Tips
- Gunakan `basename` dalam skrip shell untuk memudahkan pengendalian nama fail.
- Pastikan untuk menggunakan sambungan yang tepat apabila menggunakan pilihan `-s` untuk mengelakkan hasil yang tidak diingini.
- `basename` berguna dalam pengendalian fail dan pemprosesan teks dalam automasi tugas.