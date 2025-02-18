# [English] Debian Almquist Shell (dash) cp Usage: Copy files and directories

## Overview
The `cp` command in the Debian Almquist Shell (dash) is used to copy files and directories from one location to another. It allows users to create duplicates of files or entire directory structures, making it an essential tool for file management.

## Usage
The basic syntax for the `cp` command is as follows:

```bash
cp [options] [source] [destination]
```

## Common Options
Here are some common options you can use with the `cp` command:

- `-r` or `--recursive`: Copy directories recursively.
- `-i` or `--interactive`: Prompt before overwriting files.
- `-u` or `--update`: Copy only when the source file is newer than the destination file or when the destination file is missing.
- `-v` or `--verbose`: Explain what is being done, showing the files being copied.
- `-a` or `--archive`: Copy files and directories while preserving attributes (like timestamps and permissions).

## Common Examples

### Copy a Single File
To copy a file named `file1.txt` to a new file named `file2.txt`:

```bash
cp file1.txt file2.txt
```

### Copy a Directory Recursively
To copy a directory named `dir1` and all its contents to a new directory named `dir2`:

```bash
cp -r dir1 dir2
```

### Prompt Before Overwriting
To copy a file and prompt before overwriting an existing file:

```bash
cp -i file1.txt file2.txt
```

### Verbose Output
To see detailed output while copying files:

```bash
cp -v file1.txt file2.txt
```

### Update Files
To copy a file only if the source is newer than the destination:

```bash
cp -u file1.txt file2.txt
```

## Tips
- Always use the `-i` option when copying files to avoid accidental overwrites.
- When copying directories, remember to use the `-r` option to ensure all contents are copied.
- Use the `-v` option for a clearer understanding of what files are being copied, especially when dealing with multiple files or directories.