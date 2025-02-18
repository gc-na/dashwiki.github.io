# [English] Debian Almquist Shell (dash) watch usage: Monitor command output over time

## Overview
The `watch` command in the Debian Almquist Shell (dash) is used to execute a specified command at regular intervals, allowing users to monitor the output of that command in real-time. This is particularly useful for observing changes in command output, such as system resource usage or file modifications.

## Usage
The basic syntax of the `watch` command is as follows:

```bash
watch [options] [arguments]
```

## Common Options
- `-n, --interval`: Specify the interval in seconds between command executions. The default is 2 seconds.
- `-d, --differences`: Highlight the differences between successive updates.
- `-t, --no-title`: Suppress the header showing the command being executed and the interval.
- `-x, --exec`: Execute the command directly without using a shell.

## Common Examples
Here are several practical examples of using the `watch` command:

1. **Monitor Disk Usage:**
   To check disk usage every 5 seconds:
   ```bash
   watch -n 5 df -h
   ```

2. **Track System Memory Usage:**
   To observe memory usage with highlighted changes:
   ```bash
   watch -d free -m
   ```

3. **Check Active Processes:**
   To see the list of running processes updated every 2 seconds:
   ```bash
   watch ps aux
   ```

4. **Monitor a Log File:**
   To watch the last 10 lines of a log file:
   ```bash
   watch tail -n 10 /var/log/syslog
   ```

5. **Check Network Connections:**
   To monitor active network connections:
   ```bash
   watch -n 1 netstat -tuln
   ```

## Tips
- Use the `-d` option to easily spot changes in the output, which can save time when monitoring dynamic data.
- Adjust the interval with `-n` to suit your needs; shorter intervals provide more real-time updates but may increase system load.
- Combine `watch` with commands that have a continuous output to effectively monitor system performance or logs.