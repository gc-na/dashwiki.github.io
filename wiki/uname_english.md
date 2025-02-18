# [English] Debian Almquist Shell (dash) uname usage: Display system information

## Overview
The `uname` command is used to display system information on Unix-like operating systems, including details about the kernel, hostname, and hardware architecture. It helps users and administrators gather essential information about the system they are working on.

## Usage
The basic syntax of the `uname` command is as follows:

```bash
uname [options] [arguments]
```

## Common Options
Here are some common options you can use with the `uname` command:

- `-a`: Displays all available system information.
- `-s`: Shows the kernel name.
- `-n`: Displays the network node hostname.
- `-r`: Outputs the kernel release.
- `-v`: Shows the kernel version.
- `-m`: Displays the machine hardware name.
- `-p`: Outputs the processor type (if available).
- `-i`: Displays the hardware platform (if available).
- `-o`: Shows the operating system name.

## Common Examples

Here are several practical examples of using the `uname` command:

1. **Display all system information:**

   ```bash
   uname -a
   ```

2. **Show the kernel name:**

   ```bash
   uname -s
   ```

3. **Display the network node hostname:**

   ```bash
   uname -n
   ```

4. **Output the kernel release:**

   ```bash
   uname -r
   ```

5. **Show the machine hardware name:**

   ```bash
   uname -m
   ```

## Tips
- Use `uname -a` for a comprehensive overview of your system in one command.
- Combine `uname` with other commands in scripts to automate system checks.
- Remember that some options may not be available on all systems, so check your system's documentation if you encounter issues.