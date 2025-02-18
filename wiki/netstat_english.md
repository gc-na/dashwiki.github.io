# [English] Debian Almquist Shell (dash) netstat Usage: Display network connections and statistics

## Overview
The `netstat` command is a powerful networking tool that displays network connections, routing tables, interface statistics, and more. It helps users monitor network activity and troubleshoot network issues.

## Usage
The basic syntax of the `netstat` command is as follows:

```
netstat [options] [arguments]
```

## Common Options
Here are some common options you can use with `netstat`:

- `-a`: Show all active connections and listening ports.
- `-t`: Display TCP connections.
- `-u`: Display UDP connections.
- `-n`: Show numerical addresses instead of resolving hostnames.
- `-l`: Show only listening sockets.
- `-p`: Show the PID and name of the program to which each socket belongs.

## Common Examples

1. **Display all active connections:**
   ```bash
   netstat -a
   ```

2. **Show only TCP connections:**
   ```bash
   netstat -t
   ```

3. **Display listening ports:**
   ```bash
   netstat -l
   ```

4. **Show numerical addresses:**
   ```bash
   netstat -n
   ```

5. **Display UDP connections with program names:**
   ```bash
   netstat -up
   ```

## Tips
- Combine options for more detailed output. For example, `netstat -tunlp` will show TCP and UDP connections along with the program names.
- Use `grep` to filter results. For instance, `netstat -a | grep LISTEN` will show only listening connections.
- Regularly check your network connections to identify any unauthorized access or unusual activity.