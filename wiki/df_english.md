# [English] Debian Almquist Shell (dash) df Usage: Display disk space usage

## Overview
The `df` command in the Debian Almquist Shell (dash) is used to report the amount of disk space used and available on file systems. It provides a summary of disk usage, helping users monitor their storage capacity.

## Usage
The basic syntax of the `df` command is as follows:

```
df [options] [arguments]
```

## Common Options
- `-h`: Human-readable format; shows sizes in KB, MB, or GB.
- `-T`: Displays the file system type.
- `-a`: Includes dummy file systems in the output.
- `-i`: Shows information about inodes instead of block usage.
- `--total`: Displays a grand total of all file systems.

## Common Examples
Here are some practical examples of using the `df` command:

1. **Basic Disk Usage**
   ```sh
   df
   ```

2. **Human-Readable Format**
   ```sh
   df -h
   ```

3. **Include File System Type**
   ```sh
   df -T
   ```

4. **Show Inode Usage**
   ```sh
   df -i
   ```

5. **Total Disk Usage Across All File Systems**
   ```sh
   df --total
   ```

## Tips
- Use the `-h` option for easier interpretation of disk space, especially on systems with large storage capacities.
- Combine options for more detailed output, such as `df -hT` to see both human-readable sizes and file system types.
- Regularly check disk usage to avoid running out of space, which can lead to system issues.