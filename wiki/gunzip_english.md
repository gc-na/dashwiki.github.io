# [English] Debian Almquist Shell (dash) gunzip Usage: Decompress gzip files

## Overview
The `gunzip` command is used to decompress files that have been compressed using the `gzip` (GNU zip) compression algorithm. It is commonly used to reduce the size of files for storage or transmission and can quickly restore them to their original form.

## Usage
The basic syntax of the `gunzip` command is as follows:

```bash
gunzip [options] [arguments]
```

## Common Options
- `-c`: Write the output to standard output instead of replacing the input files.
- `-f`: Force decompression, even if the file has multiple links or is not a valid gzip file.
- `-k`: Keep the original compressed file after decompression.
- `-q`: Suppress all warnings and error messages.
- `-r`: Recursively decompress files in directories.

## Common Examples

1. **Decompress a single file:**
   ```bash
   gunzip file.txt.gz
   ```

2. **Decompress and keep the original file:**
   ```bash
   gunzip -k file.txt.gz
   ```

3. **Decompress multiple files at once:**
   ```bash
   gunzip file1.gz file2.gz file3.gz
   ```

4. **Decompress a file and write output to standard output:**
   ```bash
   gunzip -c file.txt.gz > output.txt
   ```

5. **Recursively decompress all `.gz` files in a directory:**
   ```bash
   gunzip -r /path/to/directory
   ```

## Tips
- Always check the size of your files before and after decompression to ensure the process completed successfully.
- Use the `-k` option if you want to keep the original compressed files for backup or future use.
- If you encounter issues with corrupted files, consider using the `-f` option to force decompression, but be cautious as this may lead to data loss.