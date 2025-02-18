# [English] Debian Almquist Shell (dash) uniq Usage equivalent: Remove duplicate lines from sorted files

## Overview
The `uniq` command in the Debian Almquist Shell (dash) is used to filter out repeated lines in a text file. It only works on sorted input, meaning that duplicates must be adjacent to be recognized and removed.

## Usage
The basic syntax of the `uniq` command is as follows:

```bash
uniq [options] [input_file] [output_file]
```

If no input file is specified, `uniq` reads from standard input.

## Common Options
- `-c`: Prefix each output line with the number of occurrences.
- `-d`: Only print duplicate lines.
- `-u`: Only print unique lines (lines that are not repeated).
- `-i`: Ignore case when comparing lines.
- `-w N`: Compare no more than N characters in lines.

## Common Examples

1. **Remove duplicates from a sorted file:**
   ```bash
   uniq sorted_file.txt
   ```

2. **Count occurrences of each line:**
   ```bash
   uniq -c sorted_file.txt
   ```

3. **Display only duplicate lines:**
   ```bash
   uniq -d sorted_file.txt
   ```

4. **Display only unique lines:**
   ```bash
   uniq -u sorted_file.txt
   ```

5. **Ignore case when filtering:**
   ```bash
   uniq -i sorted_file.txt
   ```

6. **Limit comparison to the first N characters:**
   ```bash
   uniq -w 5 sorted_file.txt
   ```

## Tips
- Always sort your input file before using `uniq` to ensure that duplicates are adjacent.
- Use the `-c` option to get a quick summary of how many times each line appears, which can be useful for data analysis.
- When working with large files, consider redirecting the output to a new file to preserve the original data. For example:
  ```bash
  uniq sorted_file.txt > unique_lines.txt
  ```