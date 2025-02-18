# [English] Debian Almquist Shell (dash) find usage equivalent: find file names

## Overview
The `find` command in the Debian Almquist Shell (dash) is a powerful utility used to search for files and directories within a specified location in the filesystem. It allows users to search based on various criteria such as name, type, size, modification date, and more.

## Usage
The basic syntax of the `find` command is as follows:

```sh
find [options] [path] [expression]
```

- **options**: Various flags that modify the behavior of the command.
- **path**: The directory path where the search will begin.
- **expression**: Conditions that specify what to search for.

## Common Options
- `-name <pattern>`: Search for files that match the specified name pattern.
- `-type <type>`: Search for files of a specific type (e.g., `f` for regular files, `d` for directories).
- `-size <n>`: Search for files of a specific size (e.g., `+100M` for files larger than 100MB).
- `-mtime <n>`: Search for files modified in the last `n` days.
- `-exec <command> {} \;`: Execute a command on each file found.

## Common Examples
Here are some practical examples of using the `find` command:

1. **Find files by name**:
   ```sh
   find /home/user -name "document.txt"
   ```

2. **Find all directories**:
   ```sh
   find /var -type d
   ```

3. **Find files larger than 1GB**:
   ```sh
   find / -size +1G
   ```

4. **Find files modified in the last 7 days**:
   ```sh
   find /tmp -mtime -7
   ```

5. **Execute a command on found files**:
   ```sh
   find /logs -name "*.log" -exec rm {} \;
   ```

## Tips
- Use quotes around patterns to prevent shell expansion.
- Combine options for more refined searches (e.g., `find /path -type f -name "*.txt"`).
- Use `-print` to display the results explicitly if needed.
- Be cautious with `-exec` commands, especially those that modify or delete files. Always test with `-print` first to see what will be affected.