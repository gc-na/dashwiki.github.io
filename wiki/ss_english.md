# [English] Debian Almquist Shell (dash) ss Usage equivalent in English: Display socket statistics

## Overview
The `ss` command is a utility in the Debian Almquist Shell (dash) used to investigate sockets. It provides detailed information about network connections, including listening and established sockets, as well as their state. This command is a powerful tool for network diagnostics and monitoring.

## Usage
The basic syntax of the `ss` command is as follows:

```bash
ss [options] [arguments]
```

## Common Options
- `-t`: Display TCP sockets.
- `-u`: Display UDP sockets.
- `-l`: Show listening sockets.
- `-p`: Show the process using the socket.
- `-n`: Show numerical addresses instead of resolving hostnames.
- `-s`: Display summary statistics.

## Common Examples
Here are some practical examples of using the `ss` command:

1. **Display all active TCP connections:**
   ```bash
   ss -t
   ```

2. **Show all listening UDP sockets:**
   ```bash
   ss -u -l
   ```

3. **List all sockets with process information:**
   ```bash
   ss -p
   ```

4. **Display all connections with numerical addresses:**
   ```bash
   ss -n
   ```

5. **Get a summary of socket statistics:**
   ```bash
   ss -s
   ```

## Tips
- Use the `-n` option to speed up the output by avoiding DNS lookups, especially in environments with many connections.
- Combine options for more specific queries, such as `ss -tunlp` to see all TCP and UDP connections along with their process IDs.
- Regularly check socket statistics to monitor network activity and troubleshoot issues effectively.