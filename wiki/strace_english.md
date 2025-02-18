# [English] Debian Almquist Shell (dash) strace Usage: Trace system calls and signals

## Overview
The `strace` command is a powerful diagnostic tool used to monitor the interactions between a program and the Linux kernel. It traces system calls made by a process, allowing users to see what files are accessed, what network connections are made, and how the program behaves at a low level. This is particularly useful for debugging and performance analysis.

## Usage
The basic syntax of the `strace` command is as follows:

```bash
strace [options] [arguments]
```

## Common Options
- `-c`: Summarize time, calls, and errors for each system call.
- `-e <expression>`: Filter the system calls to trace based on the provided expression.
- `-o <file>`: Write the output to the specified file instead of standard error.
- `-p <pid>`: Attach to the process with the specified process ID.
- `-f`: Trace child processes as they are created.

## Common Examples
Here are some practical examples of how to use `strace`:

1. **Trace a command and display system calls:**
   ```bash
   strace ls
   ```

2. **Trace a command and save the output to a file:**
   ```bash
   strace -o output.txt ls
   ```

3. **Summarize system calls made by a command:**
   ```bash
   strace -c ls
   ```

4. **Attach to a running process:**
   ```bash
   strace -p 1234
   ```

5. **Filter to trace only file-related system calls:**
   ```bash
   strace -e trace=file ls
   ```

## Tips
- Use `-c` to get a quick summary of system calls, which can help identify performance bottlenecks.
- When debugging, redirect the output to a file for easier analysis, especially for commands that generate a lot of output.
- Combine `strace` with other tools like `grep` to filter specific system calls or errors for more focused troubleshooting.