# [English] Debian Almquist Shell (dash) traceroute6 Usage: Trace IPv6 network paths

## Overview
The `traceroute6` command is a network diagnostic tool used to trace the path that packets take from your machine to a specified destination over an IPv6 network. It helps identify the route and measure transit delays of packets across the network, which can be useful for troubleshooting connectivity issues.

## Usage
The basic syntax of the `traceroute6` command is as follows:

```bash
traceroute6 [options] [destination]
```

## Common Options
- `-m <max_ttl>`: Set the maximum time-to-live (TTL) for the packets. This limits the number of hops the traceroute will attempt.
- `-p <port>`: Specify the destination port to use for the probe packets. Default is 33434.
- `-n`: Do not resolve hostnames, showing only IP addresses instead.
- `-w <timeout>`: Set the timeout for each probe in seconds. Default is 5 seconds.
- `-q <nqueries>`: Set the number of probe queries per hop. Default is 3.

## Common Examples
Here are some practical examples of using `traceroute6`:

1. **Basic traceroute to a destination:**
   ```bash
   traceroute6 google.com
   ```

2. **Traceroute with a specified maximum TTL:**
   ```bash
   traceroute6 -m 20 google.com
   ```

3. **Traceroute without resolving hostnames:**
   ```bash
   traceroute6 -n google.com
   ```

4. **Traceroute with a custom destination port:**
   ```bash
   traceroute6 -p 80 google.com
   ```

5. **Traceroute with a specified timeout:**
   ```bash
   traceroute6 -w 2 google.com
   ```

## Tips
- Use the `-n` option if you want faster results without the delay of DNS lookups.
- Adjust the `-m` option to limit the number of hops if you are only interested in a specific segment of the route.
- If you encounter issues with timeouts, consider increasing the `-w` timeout value to allow more time for responses.
- Regularly check the network path to critical services to monitor for changes or disruptions.