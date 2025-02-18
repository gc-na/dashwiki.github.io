# [English] Debian Almquist Shell (dash) telnet usage: Connect to remote servers

## Overview
The `telnet` command is a user interface to the TELNET protocol, which allows users to connect to remote servers over a network. It is often used for testing and debugging network services, as well as for accessing remote systems.

## Usage
The basic syntax of the `telnet` command is as follows:

```bash
telnet [options] [hostname] [port]
```

## Common Options
- `-l username`: Specify the username to log in with.
- `-d`: Enable debugging mode, which provides detailed output for troubleshooting.
- `-n tracefile`: Log all input and output to the specified trace file.
- `-e escapechar`: Set a custom escape character for telnet commands.

## Common Examples
Here are some practical examples of using the `telnet` command:

1. **Connect to a remote server:**
   ```bash
   telnet example.com
   ```

2. **Connect to a specific port on a remote server:**
   ```bash
   telnet example.com 80
   ```

3. **Log in with a specific username:**
   ```bash
   telnet -l user example.com
   ```

4. **Enable debugging mode:**
   ```bash
   telnet -d example.com
   ```

5. **Connect to a server and log the session:**
   ```bash
   telnet -n session.log example.com
   ```

## Tips
- Always ensure that the telnet service is running on the remote server before attempting to connect.
- Use telnet primarily for testing purposes, as it does not encrypt data, making it insecure for sensitive information.
- Consider using SSH for secure remote connections instead of telnet.