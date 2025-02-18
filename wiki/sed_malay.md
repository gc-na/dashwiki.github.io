# [Sistem Operasi] Debian Almquist Shell (dash) sed Penggunaan: Mengedit teks dalam aliran

## Overview
Perintah `sed` (stream editor) digunakan untuk memanipulasi dan mengedit teks dalam aliran. Ia membolehkan pengguna melakukan pelbagai operasi seperti menggantikan, menghapus, dan menyisipkan teks dalam fail atau input standard.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `sed`:

```bash
sed [options] [arguments]
```

## Common Options
- `-e`: Menentukan ekspresi pengeditan.
- `-f`: Mengambil arahan pengeditan dari fail.
- `-i`: Mengedit fail secara langsung (in-place).
- `-n`: Menghalang output secara automatik; hanya output yang ditentukan dengan `p` akan ditunjukkan.

## Common Examples

### Menggantikan teks
Untuk menggantikan semua kemunculan "lama" dengan "baru" dalam fail `contoh.txt`:

```bash
sed 's/lama/baru/g' contoh.txt
```

### Mengedit fail secara langsung
Untuk menggantikan "lama" dengan "baru" dan menyimpan perubahan dalam `contoh.txt`:

```bash
sed -i 's/lama/baru/g' contoh.txt
```

### Menghapus baris tertentu
Untuk menghapus baris ke-2 dalam fail `contoh.txt`:

```bash
sed '2d' contoh.txt
```

### Menyisipkan baris
Untuk menyisipkan "Baris baru" selepas baris ke-3 dalam fail `contoh.txt`:

```bash
sed '3a Baris baru' contoh.txt
```

## Tips
- Selalu buat salinan fail asal sebelum menggunakan `-i` untuk mengelakkan kehilangan data.
- Gunakan `-n` bersama dengan `p` untuk mengeluarkan hanya baris yang anda ingin lihat.
- Eksperimen dengan ekspresi reguler untuk pengeditan yang lebih kompleks dan berkuasa.