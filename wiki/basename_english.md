# [English] Debian Almquist Shell (dash) basename usage: Extract the filename from a path

## Overview
The `basename` command in the Debian Almquist Shell (dash) is used to strip the directory and suffix from file names. It is particularly useful when you want to obtain just the file name from a full path or remove a specific suffix from a file name.

## Usage
The basic syntax of the `basename` command is as follows:

```bash
basename [options] [arguments]
```

## Common Options
- `-a`: Treat each argument as a separate file name and return the base name for each.
- `-s`: Remove a specified suffix from the file name.
- `--help`: Display help information about the command.

## Common Examples

1. **Extracting the file name from a path:**
   ```bash
   basename /usr/local/bin/script.sh
   ```
   Output:
   ```
   script.sh
   ```

2. **Removing a suffix from a file name:**
   ```bash
   basename report.txt .txt
   ```
   Output:
   ```
   report
   ```

3. **Handling multiple file names:**
   ```bash
   basename -a /path/to/file1.txt /path/to/file2.log
   ```
   Output:
   ```
   file1.txt
   file2.log
   ```

4. **Using with a suffix:**
   ```bash
   basename -s .log /path/to/file2.log
   ```
   Output:
   ```
   file2
   ```

## Tips
- Use `basename` in scripts to dynamically extract file names from paths, which can be useful for logging or processing files.
- Combine `basename` with other commands like `find` to manipulate file names effectively.
- Remember that `basename` only returns the last component of a path; if you need to work with directories, consider using the `dirname` command.