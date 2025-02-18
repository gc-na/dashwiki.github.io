# [Sistem Operasi] Debian Almquist Shell (dash) time <Penggunaan setara>: Mengukur masa pelaksanaan arahan

## Overview
Arahan `time` digunakan untuk mengukur masa yang diambil untuk melaksanakan arahan lain dalam terminal. Ia memberikan maklumat tentang masa CPU yang digunakan dan masa keseluruhan yang diambil untuk menjalankan arahan tersebut.

## Usage
Sintaks asas bagi arahan `time` adalah seperti berikut:

```
time [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa untuk arahan `time`:

- `-p`: Menunjukkan output dalam format POSIX yang lebih ringkas.
- `-o <file>`: Menyimpan output masa ke dalam fail yang ditentukan.
- `-v`: Menunjukkan maklumat terperinci tentang penggunaan sumber.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan arahan `time`:

1. Mengukur masa untuk menjalankan arahan `ls`:
   ```sh
   time ls
   ```

2. Menggunakan pilihan `-p` untuk output ringkas:
   ```sh
   time -p sleep 2
   ```

3. Menyimpan output masa ke dalam fail:
   ```sh
   time -o output.txt sleep 3
   ```

4. Menggunakan pilihan `-v` untuk maklumat terperinci:
   ```sh
   time -v find / -name "*.txt"
   ```

## Tips
- Gunakan pilihan `-o` untuk menyimpan hasil masa ke dalam fail jika anda ingin merujuknya kemudian.
- Untuk analisis yang lebih mendalam, pilihan `-v` memberikan maklumat tambahan yang berguna.
- Pastikan untuk menggunakan `time` dengan arahan yang memerlukan masa pelaksanaan yang ketara untuk mendapatkan hasil yang lebih bermakna.