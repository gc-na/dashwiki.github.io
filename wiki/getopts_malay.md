# [Sistem Operasi] Debian Almquist Shell (dash) getopts: [mengendalikan pilihan skrip]

## Overview
Perintah `getopts` digunakan dalam skrip shell untuk memproses pilihan dan argumen yang diberikan kepada skrip. Ia membolehkan pengguna untuk menangkap dan mengendalikan pilihan yang diambil dari baris perintah dengan cara yang teratur dan mudah.

## Usage
Berikut adalah sintaks asas untuk menggunakan `getopts`:

```sh
getopts [options] [arguments]
```

## Common Options
- `-a`: Menggunakan pilihan yang ditentukan dalam argumen.
- `-b`: Menetapkan pilihan untuk pemprosesan.
- `-c`: Menunjukkan pilihan yang boleh diambil.

## Common Examples

### Contoh 1: Menggunakan `getopts` untuk pilihan tunggal
```sh
#!/bin/sh
while getopts "a:" opt; do
  case $opt in
    a)
      echo "Pilihan A: $OPTARG"
      ;;
    *)
      echo "Pilihan tidak sah"
      ;;
  esac
done
```

### Contoh 2: Menggunakan `getopts` untuk beberapa pilihan
```sh
#!/bin/sh
while getopts "a:b:c:" opt; do
  case $opt in
    a)
      echo "Pilihan A: $OPTARG"
      ;;
    b)
      echo "Pilihan B: $OPTARG"
      ;;
    c)
      echo "Pilihan C: $OPTARG"
      ;;
    *)
      echo "Pilihan tidak sah"
      ;;
  esac
done
```

### Contoh 3: Menangani pilihan tanpa argumen
```sh
#!/bin/sh
while getopts "abc" opt; do
  case $opt in
    a)
      echo "Pilihan A dipilih"
      ;;
    b)
      echo "Pilihan B dipilih"
      ;;
    c)
      echo "Pilihan C dipilih"
      ;;
    *)
      echo "Pilihan tidak sah"
      ;;
  esac
done
```

## Tips
- Sentiasa gunakan `case` untuk mengendalikan pilihan yang berbeza dengan jelas.
- Gunakan `OPTARG` untuk mendapatkan nilai argumen yang berkaitan dengan pilihan.
- Pastikan untuk menguji skrip anda dengan pelbagai kombinasi pilihan untuk memastikan ia berfungsi dengan baik.