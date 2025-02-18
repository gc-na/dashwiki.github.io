# [English] Debian Almquist Shell (dash) rmdir Usage: Remove empty directories

## Overview
The `rmdir` command in the Debian Almquist Shell (dash) is used to remove empty directories from the filesystem. If the directory contains files or other directories, the command will fail, ensuring that only truly empty directories are deleted.

## Usage
The basic syntax of the `rmdir` command is as follows:

```
rmdir [options] [arguments]
```

## Common Options
- `--ignore-fail-on-non-empty`: Ignore non-empty directories and do not display an error message.
- `--verbose`: Provide detailed output about the directories being removed.

## Common Examples
Here are some practical examples of using the `rmdir` command:

1. **Remove a single empty directory:**
   ```bash
   rmdir my_empty_directory
   ```

2. **Remove multiple empty directories at once:**
   ```bash
   rmdir dir1 dir2 dir3
   ```

3. **Use the verbose option to see output:**
   ```bash
   rmdir --verbose my_empty_directory
   ```

4. **Ignore non-empty directories:**
   ```bash
   rmdir --ignore-fail-on-non-empty my_non_empty_directory
   ```

## Tips
- Always ensure that the directory is empty before using `rmdir`, as it will not remove directories containing files or subdirectories.
- Use the `--verbose` option for confirmation when removing directories, especially when working with multiple directories.
- Consider using `rm -r` if you need to remove directories that are not empty, but be cautious as this command will delete all contents within the directory.