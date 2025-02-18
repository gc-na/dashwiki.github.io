# [Debian] Debian Almquist Shell (dash) date: [menunjukkan tarikh dan masa]

## Overview
Perintah `date` dalam shell Debian Almquist (dash) digunakan untuk memaparkan atau menetapkan tarikh dan masa sistem. Ia membolehkan pengguna untuk melihat maklumat waktu semasa dan juga untuk mengubah format paparan waktu.

## Usage
Sintaks asas untuk perintah `date` adalah seperti berikut:

```
date [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan umum yang boleh digunakan dengan perintah `date`:

- `+FORMAT`: Mengubah format output tarikh dan masa.
- `-u`: Memaparkan waktu dalam format UTC (Coordinated Universal Time).
- `-d STRING`: Menggunakan STRING untuk menentukan tarikh dan masa yang ingin dipaparkan.
- `-s STRING`: Menetapkan tarikh dan masa sistem kepada STRING yang diberikan.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `date`:

1. **Menunjukkan tarikh dan masa semasa:**
   ```bash
   date
   ```

2. **Menunjukkan tarikh dalam format tertentu:**
   ```bash
   date "+%Y-%m-%d %H:%M:%S"
   ```

3. **Menunjukkan waktu dalam format UTC:**
   ```bash
   date -u
   ```

4. **Menetapkan tarikh dan masa sistem:**
   ```bash
   sudo date -s "2023-10-01 12:00:00"
   ```

5. **Menunjukkan tarikh yang ditentukan:**
   ```bash
   date -d "next Friday"
   ```

## Tips
- Sentiasa gunakan format yang tepat untuk output yang lebih mudah dibaca.
- Pastikan anda mempunyai hak akses yang diperlukan apabila menetapkan tarikh dan masa sistem.
- Gunakan pilihan `-u` untuk memaparkan waktu dalam UTC jika anda bekerja dengan pelayan yang berada di zon waktu berbeza.