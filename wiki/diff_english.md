# [English] Debian Almquist Shell (dash) diff usage: Compare files line by line

## Overview
The `diff` command is used to compare the contents of two files line by line. It outputs the differences between the files, allowing users to see what has changed, been added, or removed. This is particularly useful for programmers and anyone who needs to track changes in text files.

## Usage
The basic syntax of the `diff` command is as follows:

```bash
diff [options] [file1] [file2]
```

## Common Options
- `-u`: Outputs the differences in a unified format, which is easier to read.
- `-c`: Provides a context diff, showing lines of context around the changes.
- `-i`: Ignores case differences in the comparison.
- `-w`: Ignores all white space when comparing lines.
- `-r`: Recursively compares any subdirectories found.

## Common Examples
Here are some practical examples of using the `diff` command:

1. **Basic Comparison**:
   Compare two text files and show the differences.
   ```bash
   diff file1.txt file2.txt
   ```

2. **Unified Format**:
   Display the differences in a unified format for better readability.
   ```bash
   diff -u file1.txt file2.txt
   ```

3. **Context Diff**:
   Show the differences along with some context lines.
   ```bash
   diff -c file1.txt file2.txt
   ```

4. **Ignoring Case**:
   Compare two files while ignoring case differences.
   ```bash
   diff -i file1.txt file2.txt
   ```

5. **Recursive Directory Comparison**:
   Compare all files in two directories recursively.
   ```bash
   diff -r dir1/ dir2/
   ```

## Tips
- Use the `-u` option for a clearer output, especially when reviewing changes.
- When working with version control systems, `diff` is often used to review changes before committing.
- For large files, consider using `diff` in combination with `less` to paginate the output: 
  ```bash
  diff file1.txt file2.txt | less
  ```
- Always check the manual page (`man diff`) for more detailed information and additional options.