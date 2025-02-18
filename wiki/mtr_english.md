# [English] Debian Almquist Shell (dash) mtr Usage: Network diagnostic tool

## Overview
The `mtr` command combines the functionality of the `traceroute` and `ping` commands to provide a comprehensive view of the network path to a destination. It helps diagnose network issues by showing the route packets take to reach a specific host, along with the latency and packet loss at each hop.

## Usage
The basic syntax of the `mtr` command is as follows:

```bash
mtr [options] [destination]
```

## Common Options
- `-r`: Run in report mode, providing a summary of the results.
- `-c <count>`: Specify the number of pings to send.
- `-i <interval>`: Set the interval between pings in seconds.
- `-w`: Use wide output format for better readability.
- `-p`: Show the port number in the output.

## Common Examples
Here are some practical examples of using the `mtr` command:

1. **Basic usage to trace a route:**
   ```bash
   mtr example.com
   ```

2. **Run in report mode with a specified number of pings:**
   ```bash
   mtr -r -c 10 example.com
   ```

3. **Set a custom interval between pings:**
   ```bash
   mtr -i 2 example.com
   ```

4. **Use wide output format for better readability:**
   ```bash
   mtr -w example.com
   ```

5. **Show the port number in the output:**
   ```bash
   mtr -p example.com
   ```

## Tips
- Use `mtr` with the `-r` option for a quick summary if you want to avoid continuous output.
- Combine the `-c` option with `-r` to limit the number of pings and get a concise report.
- If diagnosing intermittent issues, consider increasing the interval with the `-i` option to reduce network load.
- Regularly check the results of `mtr` to identify any persistent latency or packet loss issues in your network.