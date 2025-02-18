# [Sistem Operasi] Debian Almquist Shell (dash) trap: [menangani sinyal dan kejadian]

## Overview
Perintah `trap` dalam shell digunakan untuk menangani sinyal dan kejadian tertentu yang terjadi selama eksekusi skrip. Dengan `trap`, Anda dapat menentukan tindakan yang harus diambil ketika sinyal tertentu diterima, seperti menghentikan skrip atau membersihkan sumber daya.

## Usage
Berikut adalah sintaks dasar dari perintah `trap`:

```sh
trap [options] [commands] [signals]
```

## Common Options
- `-l`: Menampilkan daftar sinyal yang tersedia.
- `-p`: Menampilkan perintah yang terpasang untuk sinyal tertentu.
- `signals`: Daftar sinyal yang ingin Anda tangani, seperti `SIGINT`, `SIGTERM`, dll.

## Common Examples

### Contoh 1: Menangani Sinyal SIGINT
Menangani sinyal interupsi (Ctrl+C) untuk membersihkan sebelum keluar.

```sh
trap 'echo "Sinyal SIGINT diterima, keluar..."; exit' SIGINT
while true; do
    echo "Menunggu sinyal..."
    sleep 1
done
```

### Contoh 2: Membersihkan File Sementara
Menghapus file sementara saat skrip dihentikan.

```sh
trap 'rm -f /tmp/tempfile; echo "File sementara dihapus."' EXIT
touch /tmp/tempfile
echo "Skrip sedang berjalan..."
sleep 10
```

### Contoh 3: Menangani Sinyal SIGTERM
Menangani sinyal terminasi untuk melakukan tindakan tertentu.

```sh
trap 'echo "Sinyal SIGTERM diterima, melakukan pembersihan."' SIGTERM
while true; do
    echo "Skrip berjalan..."
    sleep 2
done
```

## Tips
- Selalu gunakan `trap` untuk menangani sinyal yang dapat menghentikan skrip Anda secara tidak terduga.
- Gunakan `trap` dengan sinyal `EXIT` untuk memastikan pembersihan dilakukan saat skrip selesai.
- Uji skrip Anda dengan mengirimkan sinyal yang berbeda untuk memastikan bahwa penanganan sinyal berfungsi dengan baik.