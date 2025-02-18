# [English] Debian Almquist Shell (dash) pidstat Usage: Monitor process statistics

## Overview
The `pidstat` command is a useful tool for monitoring individual process statistics in real-time. It provides information about CPU usage, memory consumption, and other performance metrics for running processes, making it an essential utility for system administrators and developers.

## Usage
The basic syntax of the `pidstat` command is as follows:

```bash
pidstat [options] [arguments]
```

## Common Options
- `-h`: Display help information.
- `-p <pid>`: Monitor a specific process by its PID (Process ID).
- `-r`: Report memory usage statistics.
- `-u`: Report CPU usage statistics.
- `-t`: Show statistics for all threads of a process.
- `-d`: Report I/O statistics.

## Common Examples

### Monitor CPU Usage of All Processes
To monitor CPU usage for all running processes, use the following command:

```bash
pidstat -u 1
```
This command will display CPU usage statistics every second.

### Monitor a Specific Process
To monitor a specific process with PID 1234, you can run:

```bash
pidstat -p 1234 1
```
This will show CPU usage statistics for the process with PID 1234 every second.

### Monitor Memory Usage
To check memory usage statistics, use the `-r` option:

```bash
pidstat -r 1
```
This command will display memory usage information for all processes every second.

### Monitor All Threads of a Process
To view statistics for all threads of a specific process, use:

```bash
pidstat -t -p 1234 1
```
This will show CPU usage for all threads of the process with PID 1234 every second.

### Monitor I/O Statistics
To monitor I/O statistics for a specific process, use the `-d` option:

```bash
pidstat -d -p 1234 1
```
This command will display I/O statistics for the process with PID 1234 every second.

## Tips
- Use the `-h` option to quickly access help and see all available options.
- Combine options for more detailed output, such as `pidstat -urd -p 1234 1` to monitor both CPU and memory usage.
- Consider redirecting output to a file for later analysis, e.g., `pidstat -u 1 > pidstat_output.txt`.