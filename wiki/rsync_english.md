# [English] Debian Almquist Shell (dash) rsync Usage equivalent in English: Synchronize files and directories

## Overview
The `rsync` command is a powerful tool used for synchronizing files and directories between two locations. It can be used locally or over a network, making it ideal for backups, mirroring, and transferring files efficiently.

## Usage
The basic syntax of the `rsync` command is as follows:

```bash
rsync [options] [source] [destination]
```

## Common Options
- `-a`: Archive mode; it preserves permissions, timestamps, symbolic links, and other file attributes.
- `-v`: Verbose output; it provides detailed information about the transfer process.
- `-z`: Compress file data during the transfer, which can speed up the process over slow connections.
- `-r`: Recursively copy directories and their contents.
- `--delete`: Delete files in the destination that are not present in the source.
- `-n`: Perform a dry run; it shows what would be done without actually making any changes.

## Common Examples
Here are some practical examples of using the `rsync` command:

1. **Basic file synchronization:**
   ```bash
   rsync -av source.txt /path/to/destination/
   ```

2. **Synchronizing a directory:**
   ```bash
   rsync -av /path/to/source/ /path/to/destination/
   ```

3. **Synchronizing over SSH:**
   ```bash
   rsync -avz -e ssh /path/to/source/ user@remote_host:/path/to/destination/
   ```

4. **Performing a dry run:**
   ```bash
   rsync -avn /path/to/source/ /path/to/destination/
   ```

5. **Deleting extraneous files in the destination:**
   ```bash
   rsync -av --delete /path/to/source/ /path/to/destination/
   ```

## Tips
- Always perform a dry run (`-n`) before executing a command that will modify or delete files, especially when using the `--delete` option.
- Use the `-z` option when transferring files over slow networks to reduce transfer time.
- Consider using `--progress` to see the progress of the transfer, especially for large files.