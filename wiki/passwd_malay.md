# [Sistem Operasi] Debian Almquist Shell (dash) passwd: [mengurus kata laluan pengguna]

## Overview
Perintah `passwd` digunakan untuk mengubah kata laluan pengguna dalam sistem. Ia membolehkan pengguna menukar kata laluan mereka sendiri atau pentadbir menukar kata laluan untuk pengguna lain.

## Usage
Berikut adalah sintaks asas untuk perintah `passwd`:

```bash
passwd [options] [arguments]
```

## Common Options
- `-d`: Padamkan kata laluan pengguna, membolehkan akses tanpa kata laluan.
- `-e`: Tandakan kata laluan pengguna sebagai tamat tempoh, memaksa pengguna untuk menukar kata laluan pada log masuk seterusnya.
- `-l`: Kunci akaun pengguna, menjadikannya tidak boleh diakses.
- `-u`: Buka kunci akaun pengguna yang telah dikunci.

## Common Examples
1. **Menukar kata laluan pengguna semasa:**
   ```bash
   passwd
   ```

2. **Menukar kata laluan untuk pengguna tertentu (perlu hak pentadbir):**
   ```bash
   passwd username
   ```

3. **Menghapuskan kata laluan pengguna:**
   ```bash
   passwd -d username
   ```

4. **Menandakan kata laluan pengguna tamat tempoh:**
   ```bash
   passwd -e username
   ```

5. **Mengunci akaun pengguna:**
   ```bash
   passwd -l username
   ```

## Tips
- Sentiasa gunakan kata laluan yang kuat dan unik untuk meningkatkan keselamatan.
- Jika anda seorang pentadbir, pastikan anda memberi amaran kepada pengguna sebelum mengunci atau menghapuskan kata laluan mereka.
- Gunakan pilihan `-e` untuk memaksa pengguna menukar kata laluan secara berkala bagi meningkatkan keselamatan.