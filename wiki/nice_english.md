# [English] Debian Almquist Shell (dash) nice usage: Adjust process priority

## Overview
The `nice` command in the Debian Almquist Shell (dash) is used to run a command with a modified scheduling priority. By default, processes run with a priority of 0, but you can increase or decrease this value using `nice`. Lowering the priority allows other processes to run more smoothly, while raising it can help ensure that your command gets more CPU time.

## Usage
The basic syntax of the `nice` command is:

```bash
nice [options] [command [arguments]]
```

## Common Options
- `-n, --adjustment=N`: Set the priority adjustment value. The default is 10, which increases the priority.
- `-h, --help`: Display help information about the command.
- `--version`: Show the version information of the `nice` command.

## Common Examples
Here are some practical examples of using the `nice` command:

1. **Run a command with default priority adjustment:**
   ```bash
   nice sleep 10
   ```
   This runs the `sleep` command for 10 seconds with a default priority adjustment of 10.

2. **Run a command with a specific priority adjustment:**
   ```bash
   nice -n 5 tar -czf backup.tar.gz /path/to/directory
   ```
   This creates a compressed archive of a directory with a priority adjustment of 5.

3. **Run a command with a negative priority adjustment (requires superuser privileges):**
   ```bash
   sudo nice -n -5 make
   ```
   This runs the `make` command with a higher priority, allowing it to use more CPU resources.

4. **Check the priority of a running process:**
   ```bash
   ps -o pid,ni,cmd | grep myprocess
   ```
   This command lists the process ID, nice value, and command for a specific process.

## Tips
- Use `nice` to improve system responsiveness when running resource-intensive tasks.
- Remember that negative priority adjustments require superuser privileges, so use `sudo` when necessary.
- Monitor your system's performance using tools like `top` or `htop` to see the effects of your priority adjustments.