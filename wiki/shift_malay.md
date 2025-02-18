# [Sistem Operasi] Debian Almquist Shell (dash) shift: Mengubah Posisi Parameter Posisi

## Overview
Perintah `shift` dalam shell digunakan untuk mengubah posisi parameter yang diterima oleh skrip atau fungsi. Dengan menggunakan `shift`, anda dapat menggeser semua parameter ke kiri, sehingga parameter kedua menjadi yang pertama, dan seterusnya. Ini berguna ketika anda ingin memproses parameter satu per satu.

## Usage
Berikut adalah sintaks asas untuk perintah `shift`:

```sh
shift [n]
```

Di mana `n` adalah bilangan yang menunjukkan berapa banyak posisi yang ingin anda geser. Jika `n` tidak ditentukan, `shift` akan menggeser satu posisi.

## Common Options
- `n`: Bilangan yang menunjukkan berapa banyak parameter yang ingin digeser. Jika tidak ditentukan, secara default `shift` akan menggeser satu posisi.

## Common Examples

### Contoh 1: Menggeser Satu Posisi
```sh
#!/bin/dash
set -- "satu" "dua" "tiga"
echo "Sebelum shift: $1 $2 $3"
shift
echo "Selepas shift: $1 $2 $3"
```
Output:
```
Sebelum shift: satu dua tiga
Selepas shift: dua tiga
```

### Contoh 2: Menggeser Dua Posisi
```sh
#!/bin/dash
set -- "satu" "dua" "tiga" "empat"
echo "Sebelum shift: $1 $2 $3 $4"
shift 2
echo "Selepas shift: $1 $2 $3 $4"
```
Output:
```
Sebelum shift: satu dua tiga empat
Selepas shift: tiga empat
```

### Contoh 3: Menggunakan dalam Skrip
```sh
#!/bin/dash
while [ "$#" -gt 0 ]; do
    echo "Parameter: $1"
    shift
done
```
Output (jika dijalankan dengan `./script.sh a b c`):
```
Parameter: a
Parameter: b
Parameter: c
```

## Tips
- Gunakan `shift` dalam skrip yang memerlukan pemprosesan parameter berulang untuk memudahkan pengendalian parameter.
- Pastikan untuk memeriksa bilangan parameter sebelum menggunakan `shift` untuk mengelakkan kesalahan jika tidak ada parameter yang tersisa.
- Anda boleh menggabungkan `shift` dengan perintah lain untuk membuat skrip yang lebih kompleks dan berfungsi dengan baik.