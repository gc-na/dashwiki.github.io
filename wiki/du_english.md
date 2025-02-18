# [English] Debian Almquist Shell (dash) du Usage: Display disk usage statistics

## Overview
The `du` command in the Debian Almquist Shell (dash) is used to estimate and display the disk space used by files and directories. It provides a way to analyze how much space is consumed on your filesystem, which can be particularly useful for managing storage.

## Usage
The basic syntax of the `du` command is as follows:

```bash
du [options] [arguments]
```

## Common Options
Here are some common options you can use with the `du` command:

- `-h`: Display sizes in a human-readable format (e.g., KB, MB).
- `-s`: Show only the total size of each argument.
- `-a`: Include files as well as directories in the output.
- `-c`: Produce a grand total at the end of the output.
- `--max-depth=N`: Limit the output to directories and files up to N levels deep.

## Common Examples

1. **Display disk usage of the current directory:**
   ```bash
   du
   ```

2. **Display disk usage in a human-readable format:**
   ```bash
   du -h
   ```

3. **Show total size of a specific directory:**
   ```bash
   du -sh /path/to/directory
   ```

4. **Include files in the output:**
   ```bash
   du -ah /path/to/directory
   ```

5. **Limit output to a specific depth:**
   ```bash
   du --max-depth=1 /path/to/directory
   ```

6. **Display a grand total of disk usage:**
   ```bash
   du -ch /path/to/directory
   ```

## Tips
- Use the `-h` option to make the output easier to read, especially when dealing with large directories.
- Combine `du` with other commands like `sort` to find the largest directories:
  ```bash
  du -h /path/to/directory | sort -hr
  ```
- Regularly check disk usage to avoid running out of space, especially on servers or systems with limited storage.