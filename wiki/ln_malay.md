# [Sistem Operasi] Debian Almquist Shell (dash) ln <Menggunakan perintah ini untuk mencipta pautan>: Mencipta pautan fail

## Overview
Perintah `ln` digunakan untuk mencipta pautan kepada fail dalam sistem fail. Terdapat dua jenis pautan yang boleh dibuat: pautan keras (hard link) dan pautan lembut (symbolic link). Pautan keras adalah satu entri dalam sistem fail yang merujuk kepada lokasi yang sama dengan fail asal, manakala pautan lembut adalah pautan yang merujuk kepada nama fail lain.

## Usage
Sintaks asas bagi perintah `ln` adalah seperti berikut:
```
ln [options] [arguments]
```

## Common Options
- `-s`: Mencipta pautan lembut (symbolic link).
- `-f`: Memaksa penggantian fail yang sedia ada.
- `-n`: Mengelakkan penggantian pautan jika pautan sedia ada adalah pautan lembut.
- `-v`: Menunjukkan maklumat tentang pautan yang dicipta.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `ln`:

1. **Mencipta pautan keras:**
   ```bash
   ln fail_asal.txt pautan_keras.txt
   ```

2. **Mencipta pautan lembut:**
   ```bash
   ln -s fail_asal.txt pautan_lembut.txt
   ```

3. **Memaksa penggantian pautan sedia ada:**
   ```bash
   ln -f pautan_keras.txt pautan_baru.txt
   ```

4. **Mencipta pautan lembut dengan maklumat:**
   ```bash
   ln -sv fail_asal.txt pautan_lembut.txt
   ```

## Tips
- Gunakan pautan lembut apabila anda ingin merujuk kepada fail yang mungkin dipindahkan atau diubah nama.
- Pautan keras tidak boleh merujuk kepada direktori dan tidak boleh merujuk kepada fail yang berada di sistem fail yang berbeza.
- Sentiasa semak sama ada pautan yang ingin anda cipta sudah wujud untuk mengelakkan kehilangan data.