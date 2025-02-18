# [Sistem Operasi] Debian Almquist Shell (dash) export: Mengurus pembolehubah persekitaran

## Overview
Perintah `export` dalam shell digunakan untuk menetapkan pembolehubah persekitaran yang boleh diakses oleh proses anak. Dengan menggunakan `export`, anda boleh memastikan bahawa pembolehubah yang anda buat dalam sesi shell semasa boleh digunakan oleh skrip atau program lain yang dijalankan dari sesi tersebut.

## Usage
Sintaks asas untuk perintah `export` adalah seperti berikut:

```sh
export [options] [arguments]
```

## Common Options
- `-n`: Menghapuskan pembolehubah daripada senarai eksport.
- `-p`: Menunjukkan semua pembolehubah persekitaran yang telah dieksport.

## Common Examples

### Menetapkan Pembolehubah Persekitaran
Untuk menetapkan pembolehubah persekitaran baru, anda boleh menggunakan:

```sh
export MY_VAR="Hello, World!"
```

### Mengakses Pembolehubah Persekitaran
Setelah anda mengeksport pembolehubah, anda boleh mengaksesnya dalam sesi shell yang sama:

```sh
echo $MY_VAR
```

### Menetapkan Pembolehubah dan Mengeksportnya Dalam Satu Baris
Anda juga boleh menetapkan dan mengeksport pembolehubah dalam satu baris:

```sh
export PATH="$PATH:/usr/local/bin"
```

### Menghapuskan Pembolehubah Persekitaran
Untuk menghapuskan pembolehubah daripada senarai eksport, gunakan:

```sh
export -n MY_VAR
```

### Menunjukkan Semua Pembolehubah Persekitaran
Untuk melihat semua pembolehubah persekitaran yang telah dieksport, gunakan:

```sh
export -p
```

## Tips
- Sentiasa gunakan huruf besar untuk nama pembolehubah persekitaran agar mudah dikenali.
- Pastikan untuk mengeksport pembolehubah yang diperlukan sebelum menjalankan skrip yang memerlukannya.
- Gunakan `export -p` untuk menyemak pembolehubah yang telah dieksport sebelum membuat perubahan.