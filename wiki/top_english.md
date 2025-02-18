# [English] Debian Almquist Shell (dash) top usage: Monitor system processes in real-time

## Overview
The `top` command is a powerful utility that provides a real-time view of the system's processes. It displays information about CPU usage, memory usage, and the processes currently running on the system, allowing users to monitor system performance and resource consumption.

## Usage
The basic syntax of the `top` command is as follows:

```bash
top [options]
```

## Common Options
- `-d seconds`: Set the delay between updates to the specified number of seconds.
- `-n iterations`: Specify the number of updates to display before exiting.
- `-u username`: Show only the processes owned by the specified user.
- `-p pid`: Monitor only the process with the specified process ID (PID).

## Common Examples
Here are some practical examples of using the `top` command:

1. **Start top with default settings:**

   ```bash
   top
   ```

2. **Update every 2 seconds:**

   ```bash
   top -d 2
   ```

3. **Show processes for a specific user:**

   ```bash
   top -u username
   ```

4. **Monitor a specific process by PID:**

   ```bash
   top -p 1234
   ```

5. **Limit the output to 5 iterations:**

   ```bash
   top -n 5
   ```

## Tips
- Use the `h` key while `top` is running to access help and learn about additional commands.
- Press `q` to exit the `top` interface quickly.
- You can sort processes by CPU or memory usage by pressing the `P` or `M` keys, respectively, while `top` is running.
- Consider using `htop` for a more user-friendly interface if it's available on your system.