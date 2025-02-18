# [English] Debian Almquist Shell (dash) mkdir Usage: Create directories

## Overview
The `mkdir` command in the Debian Almquist Shell (dash) is used to create new directories in the file system. It allows users to organize files and directories efficiently by creating a structured hierarchy.

## Usage
The basic syntax of the `mkdir` command is as follows:

```bash
mkdir [options] [arguments]
```

## Common Options
- `-p`: Create parent directories as needed. If the specified directory's parent does not exist, it will be created.
- `-m`: Set the file mode (permissions) for the new directory. This option allows you to specify the permissions in octal format.
- `--help`: Display help information about the command and its options.

## Common Examples
Here are some practical examples of using the `mkdir` command:

1. **Create a single directory:**
   ```bash
   mkdir my_directory
   ```

2. **Create multiple directories at once:**
   ```bash
   mkdir dir1 dir2 dir3
   ```

3. **Create a directory with specific permissions:**
   ```bash
   mkdir -m 755 my_secure_directory
   ```

4. **Create a nested directory structure:**
   ```bash
   mkdir -p parent_dir/child_dir/grandchild_dir
   ```

5. **Create multiple nested directories:**
   ```bash
   mkdir -p project/{src,bin,docs}
   ```

## Tips
- Always use the `-p` option when creating nested directories to avoid errors if the parent directory does not exist.
- Check the permissions of the newly created directory using the `ls -l` command to ensure they are set as intended.
- Use meaningful names for directories to make navigation easier and to maintain organization within your file system.