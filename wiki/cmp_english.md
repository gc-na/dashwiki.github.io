# [English] Debian Almquist Shell (dash) cmp Usage: Compare two files byte by byte

## Overview
The `cmp` command in the Debian Almquist Shell (dash) is used to compare two files byte by byte. It identifies the first byte where the files differ and can also report the location of the differences. This command is particularly useful for verifying file integrity and ensuring that two files are identical.

## Usage
The basic syntax of the `cmp` command is as follows:

```bash
cmp [options] [file1] [file2]
```

## Common Options
- `-l`: Print the differing bytes in octal format.
- `-s`: Suppress all output; only return the exit status.
- `-i OFFSET`: Skip the first OFFSET bytes of the input files.
- `-n N`: Compare only the first N bytes of the files.

## Common Examples

### Example 1: Basic Comparison
To compare two files and see if they differ:

```bash
cmp file1.txt file2.txt
```

### Example 2: Suppress Output
To check if two files are identical without any output:

```bash
cmp -s file1.txt file2.txt
```
You can check the exit status afterwards to determine if they are the same (exit status 0) or different (exit status 1).

### Example 3: Show Differences in Octal
To display the differing bytes in octal format:

```bash
cmp -l file1.txt file2.txt
```

### Example 4: Compare a Specific Number of Bytes
To compare only the first 100 bytes of two files:

```bash
cmp -n 100 file1.txt file2.txt
```

## Tips
- Use the `-s` option if you only need to check if files are the same without cluttering your terminal with output.
- When comparing binary files, `cmp` is often more efficient than `diff`, as it focuses on byte-level differences.
- Always check the exit status of `cmp` when using the `-s` option to determine the result of the comparison.