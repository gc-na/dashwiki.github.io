# [Debian] Debian Almquist Shell (dash) ping6 Uso: Testar conectividade IPv6

## Overview
The `ping6` command is used to test the reachability of a host on an Internet Protocol version 6 (IPv6) network. It sends Internet Control Message Protocol (ICMP) Echo Request messages to the specified address and listens for Echo Response replies, helping to diagnose network connectivity issues.

## Usage
The basic syntax of the `ping6` command is as follows:

```bash
ping6 [options] [arguments]
```

## Common Options
- `-c <count>`: Stop after sending a specified number of packets.
- `-i <interval>`: Wait a specified number of seconds between sending each packet.
- `-t <ttl>`: Set the Time to Live for the packets.
- `-W <timeout>`: Set a timeout for waiting for a response.

## Common Examples
Here are some practical examples of using the `ping6` command:

1. **Ping a specific IPv6 address:**
   ```bash
   ping6 2001:db8::1
   ```

2. **Ping a hostname using IPv6:**
   ```bash
   ping6 example.com
   ```

3. **Send a specific number of packets:**
   ```bash
   ping6 -c 5 2001:db8::1
   ```

4. **Set an interval of 2 seconds between packets:**
   ```bash
   ping6 -i 2 2001:db8::1
   ```

5. **Set a timeout of 1 second for responses:**
   ```bash
   ping6 -W 1 2001:db8::1
   ```

## Tips
- Use the `-c` option to limit the number of packets sent, which is useful for quick tests.
- Combine options for more control, such as setting both the count and interval.
- If you are troubleshooting, consider using the `-t` option to adjust the TTL and see how far packets are traveling in the network.