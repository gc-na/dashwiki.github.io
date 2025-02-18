# [English] Debian Almquist Shell (dash) iotop Usage: Monitor disk I/O usage by processes

## Overview
The `iotop` command is a powerful tool for monitoring disk I/O usage by processes in real-time. It provides a dynamic view of which processes are consuming the most disk bandwidth, making it easier to identify performance bottlenecks related to disk activity.

## Usage
The basic syntax of the `iotop` command is as follows:

```bash
iotop [options] [arguments]
```

## Common Options
- `-o`, `--only`: Show only processes or threads actually doing I/O, which can help filter out idle processes.
- `-b`, `--batch`: Run in batch mode, useful for logging output to a file.
- `-n NUM`, `--iter=NUM`: Set the number of iterations before exiting. Useful for limiting the output.
- `-d SEC`, `--delay=SEC`: Set the delay between updates in seconds. Adjusts how often the display refreshes.

## Common Examples
Here are some practical examples of using `iotop`:

1. **Basic Usage**: To start monitoring disk I/O usage:
   ```bash
   iotop
   ```

2. **Show Only Processes Doing I/O**: To filter and show only processes that are currently performing I/O:
   ```bash
   iotop -o
   ```

3. **Batch Mode for Logging**: To log the output to a file every 2 seconds for 5 iterations:
   ```bash
   iotop -b -n 5 -d 2 > iotop_log.txt
   ```

4. **Longer Delay Between Updates**: To set a longer delay of 5 seconds between updates:
   ```bash
   iotop -d 5
   ```

## Tips
- Use `iotop` with root privileges to see all processes, as some may be restricted without elevated permissions.
- Combine `iotop` with other monitoring tools like `htop` for comprehensive system performance analysis.
- Regularly check disk I/O usage if you notice slowdowns in system performance, as it can help identify problematic processes.