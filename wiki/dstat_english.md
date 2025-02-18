# [English] Debian Almquist Shell (dash) dstat Usage: Monitor system resources in real-time

## Overview
The `dstat` command is a versatile tool used to monitor system resources in real-time. It combines the functionality of various monitoring tools and provides a comprehensive overview of system performance, including CPU usage, memory consumption, disk activity, and network statistics.

## Usage
The basic syntax of the `dstat` command is as follows:

```bash
dstat [options] [arguments]
```

## Common Options
- `-c`: Show CPU statistics.
- `-d`: Display disk statistics.
- `-n`: Show network statistics.
- `-m`: Monitor memory usage.
- `-t`: Include a timestamp in the output.
- `--help`: Display help information about the command and its options.

## Common Examples
Here are some practical examples of using the `dstat` command:

1. **Basic CPU and Disk Usage Monitoring**
   ```bash
   dstat -cd
   ```

2. **Monitor CPU, Memory, and Network Statistics**
   ```bash
   dstat -cnm
   ```

3. **Display All Available Statistics with Timestamps**
   ```bash
   dstat -tcdmn
   ```

4. **Monitor Disk Activity Only**
   ```bash
   dstat -d
   ```

5. **Run dstat for a Specific Duration (e.g., 10 seconds)**
   ```bash
   dstat 10
   ```

## Tips
- Use the `-t` option to include timestamps, which can help correlate events with system performance.
- Combine multiple options to get a more comprehensive view of your system's performance.
- Consider redirecting the output to a file for later analysis, using `dstat > output.txt`.
- Use `--help` to explore additional options and customize the output to your needs.