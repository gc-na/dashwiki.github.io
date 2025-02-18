# [Sistem Operasi] Debian Almquist Shell (dash) mount: [pasang sistem fail]

## Overview
Perintah `mount` digunakan untuk memasang sistem fail ke dalam direktori tertentu dalam sistem Linux. Dengan menggunakan `mount`, pengguna dapat mengakses fail dan direktori yang terdapat dalam sistem fail yang berbeza, seperti pemacu USB, partition lain, atau sistem fail rangkaian.

## Usage
Berikut adalah sintaks asas untuk perintah `mount`:

```
mount [options] [arguments]
```

## Common Options
- `-t type` : Menentukan jenis sistem fail yang akan dipasang (contohnya, ext4, ntfs).
- `-o options` : Menyediakan pilihan tambahan seperti read-only (`ro`) atau read-write (`rw`).
- `-a` : Memasang semua sistem fail yang ditentukan dalam `/etc/fstab`.
- `-r` : Memasang sistem fail dalam mod baca sahaja.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan perintah `mount`:

1. **Memasang pemacu USB**:
   ```bash
   mount /dev/sdb1 /mnt/usb
   ```

2. **Memasang sistem fail dengan jenis tertentu**:
   ```bash
   mount -t ext4 /dev/sda1 /mnt/data
   ```

3. **Memasang sistem fail dalam mod baca sahaja**:
   ```bash
   mount -o ro /dev/sda2 /mnt/backup
   ```

4. **Memasang semua sistem fail yang ditentukan dalam fstab**:
   ```bash
   mount -a
   ```

## Tips
- Sentiasa pastikan untuk mencabut sistem fail dengan perintah `umount` sebelum mencabut pemacu fizikal untuk mengelakkan kerosakan data.
- Gunakan perintah `df -h` untuk memeriksa sistem fail yang sedang dipasang dan ruang yang tersedia.
- Jika anda tidak pasti jenis sistem fail, anda boleh menggunakan perintah `blkid` untuk mendapatkan maklumat lanjut tentang partition.