# [English] Debian Almquist Shell (dash) comm: Compare sorted files line by line

## Overview
The `comm` command in the Debian Almquist Shell (dash) is used to compare two sorted files line by line. It outputs the lines that are unique to each file and the lines that are common to both files. This is particularly useful for identifying differences and similarities between two datasets.

## Usage
The basic syntax of the `comm` command is as follows:

```bash
comm [options] [file1] [file2]
```

## Common Options
- `-1`: Suppress the output of lines unique to the first file.
- `-2`: Suppress the output of lines unique to the second file.
- `-3`: Suppress the output of lines that are common to both files.
- `-i`: Ignore case when comparing lines.
- `-u`: Print only unique lines from both files.

## Common Examples

1. **Basic comparison of two files:**
   ```bash
   comm file1.txt file2.txt
   ```

2. **Suppress lines unique to the first file:**
   ```bash
   comm -1 file1.txt file2.txt
   ```

3. **Suppress lines unique to the second file:**
   ```bash
   comm -2 file1.txt file2.txt
   ```

4. **Suppress lines that are common to both files:**
   ```bash
   comm -3 file1.txt file2.txt
   ```

5. **Case-insensitive comparison:**
   ```bash
   comm -i file1.txt file2.txt
   ```

6. **Show only unique lines from both files:**
   ```bash
   comm -u file1.txt file2.txt
   ```

## Tips
- Ensure that the files are sorted before using `comm`, as it requires sorted input to function correctly.
- Use the `sort` command to sort files if they are not already sorted:
  ```bash
  sort file1.txt -o file1.txt
  sort file2.txt -o file2.txt
  ```
- Combine `comm` with other commands in a pipeline for more complex data processing tasks.