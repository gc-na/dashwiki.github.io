# [English] Debian Almquist Shell (dash) dig <Usage equivalent in English>: Query DNS information

## Overview
The `dig` command, short for Domain Information Groper, is a powerful tool used for querying DNS (Domain Name System) servers. It helps users retrieve information about domain names, such as IP addresses, mail servers, and other DNS records.

## Usage
The basic syntax of the `dig` command is as follows:

```
dig [options] [arguments]
```

## Common Options
- `@server`: Specifies the DNS server to query.
- `-t type`: Defines the type of DNS record to retrieve (e.g., A, MX, TXT).
- `+short`: Provides a concise output, showing only the answer section.
- `-x address`: Performs a reverse lookup, converting an IP address to a domain name.
- `+trace`: Traces the delegation path from the root DNS servers to the authoritative server.

## Common Examples
Here are some practical examples of using the `dig` command:

1. **Querying an A record**:
   ```bash
   dig example.com
   ```

2. **Querying a specific DNS record type (MX)**:
   ```bash
   dig -t MX example.com
   ```

3. **Using a specific DNS server**:
   ```bash
   dig @8.8.8.8 example.com
   ```

4. **Performing a reverse DNS lookup**:
   ```bash
   dig -x 8.8.8.8
   ```

5. **Getting a short answer**:
   ```bash
   dig +short example.com
   ```

6. **Tracing the DNS resolution path**:
   ```bash
   dig +trace example.com
   ```

## Tips
- Use the `+short` option for quick lookups when you only need the answer.
- When troubleshooting DNS issues, the `+trace` option can help you understand where the resolution process is failing.
- Always specify a DNS server with the `@server` option if you want to test against a specific server, especially if you suspect local DNS caching issues.