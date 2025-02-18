# [Sistem Operasi] Debian Almquist Shell (dash) unset: [hapus pembolehubah]

## Overview
Perintah `unset` dalam shell Debian Almquist (dash) digunakan untuk menghapus pembolehubah persekitaran atau pembolehubah yang ditakrifkan dalam sesi shell semasa. Ini berguna untuk menguruskan ruang nama pembolehubah dan memastikan bahawa pembolehubah yang tidak lagi diperlukan tidak lagi wujud.

## Usage
Sintaks asas untuk perintah `unset` adalah seperti berikut:

```
unset [options] [arguments]
```

## Common Options
- `-f`: Menghapus fungsi shell yang ditakrifkan.
- `-v`: Menghapus pembolehubah biasa.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `unset`:

1. **Menghapus pembolehubah biasa:**
   ```sh
   MY_VAR="Hello, World!"
   echo $MY_VAR  # Output: Hello, World!
   unset MY_VAR
   echo $MY_VAR  # Output: (tiada output)
   ```

2. **Menghapus fungsi shell:**
   ```sh
   my_function() {
       echo "This is a function."
   }
   my_function  # Output: This is a function.
   unset -f my_function
   my_function  # Output: (tiada output)
   ```

3. **Menghapus beberapa pembolehubah sekaligus:**
   ```sh
   VAR1="Value 1"
   VAR2="Value 2"
   unset VAR1 VAR2
   echo $VAR1 $VAR2  # Output: (tiada output)
   ```

## Tips
- Sentiasa periksa pembolehubah yang ingin dihapuskan untuk mengelakkan kehilangan data yang penting.
- Gunakan `unset -f` dengan berhati-hati, kerana menghapus fungsi shell boleh menyebabkan skrip yang bergantung kepada fungsi tersebut gagal.
- Untuk mengelakkan konflik nama, gunakan nama pembolehubah yang unik dan deskriptif.