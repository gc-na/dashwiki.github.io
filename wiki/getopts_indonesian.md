# [Indonesian] Debian Almquist Shell (dash) getopts: Mengelola opsi skrip

## Overview
Perintah `getopts` digunakan dalam skrip shell untuk mengelola opsi dan argumen yang diberikan kepada skrip. Ini memudahkan pemrogram untuk menangani input dari pengguna dengan cara yang terstruktur.

## Usage
Berikut adalah sintaks dasar dari perintah `getopts`:

```sh
getopts [options] [arguments]
```

## Common Options
- `-a`: Mengatur opsi untuk mengizinkan beberapa argumen.
- `-n`: Menentukan nama skrip yang akan ditampilkan dalam pesan kesalahan.
- `-s`: Menyembunyikan output kesalahan.

## Common Examples

### Contoh 1: Opsi Tunggal
Skrip berikut menggunakan `getopts` untuk menangani opsi `-f`:

```sh
#!/bin/dash
while getopts "f:" opt; do
  case $opt in
    f)
      echo "File yang diberikan: $OPTARG"
      ;;
    \?)
      echo "Opsi tidak valid: -$OPTARG" >&2
      ;;
  esac
done
```

### Contoh 2: Beberapa Opsi
Skrip ini menangani beberapa opsi `-a` dan `-b`:

```sh
#!/bin/dash
while getopts "ab:" opt; do
  case $opt in
    a)
      echo "Opsi A diaktifkan"
      ;;
    b)
      echo "Opsi B dengan argumen: $OPTARG"
      ;;
    \?)
      echo "Opsi tidak valid: -$OPTARG" >&2
      ;;
  esac
done
```

### Contoh 3: Menangani Kesalahan
Skrip ini menunjukkan cara menangani kesalahan dengan `getopts`:

```sh
#!/bin/dash
while getopts "x:y:" opt; do
  case $opt in
    x)
      echo "Opsi X dengan argumen: $OPTARG"
      ;;
    y)
      echo "Opsi Y dengan argumen: $OPTARG"
      ;;
    \?)
      echo "Opsi tidak valid: -$OPTARG" >&2
      exit 1
      ;;
  esac
done
```

## Tips
- Selalu gunakan `case` untuk menangani opsi dan argumen dengan jelas.
- Gunakan `OPTARG` untuk mendapatkan nilai argumen dari opsi.
- Pastikan untuk menangani opsi yang tidak valid untuk meningkatkan pengalaman pengguna.