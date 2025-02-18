# [English] Debian Almquist Shell (dash) head Usage: Display the beginning of a file

## Overview
The `head` command in the Debian Almquist Shell (dash) is used to display the first few lines of a file. It is particularly useful for quickly viewing the beginning of large files without opening the entire file.

## Usage
The basic syntax of the `head` command is as follows:

```bash
head [options] [arguments]
```

## Common Options
- `-n NUM`: Display the first `NUM` lines of each file. If `NUM` is omitted, the default is 10 lines.
- `-c NUM`: Display the first `NUM` bytes of each file.
- `-q`: Suppress the output of file headers when multiple files are specified.
- `-v`: Always print headers giving file names.

## Common Examples
Here are some practical examples of using the `head` command:

1. Display the first 10 lines of a file:
   ```bash
   head filename.txt
   ```

2. Display the first 5 lines of a file:
   ```bash
   head -n 5 filename.txt
   ```

3. Display the first 20 bytes of a file:
   ```bash
   head -c 20 filename.txt
   ```

4. Display the first 10 lines of multiple files:
   ```bash
   head file1.txt file2.txt
   ```

5. Display the first 10 lines without file headers:
   ```bash
   head -q file1.txt file2.txt
   ```

## Tips
- Use `head` in combination with other commands, such as `grep`, to filter and view specific sections of large files.
- If you frequently need to view more than 10 lines, consider creating an alias in your shell configuration file to adjust the default behavior.
- Remember that `head` reads from the beginning of the file, so it is efficient for quickly checking file contents without loading the entire file.