# [Debian] Debian Almquist Shell (dash) nslookup uso: Query DNS information

## Overview
The `nslookup` command is a network utility used to query Domain Name System (DNS) servers to obtain domain name or IP address mapping, or other DNS records. It helps users troubleshoot DNS-related issues by providing information about the DNS records associated with a domain.

## Usage
The basic syntax of the `nslookup` command is as follows:

```bash
nslookup [options] [arguments]
```

## Common Options
- `-type=TYPE`: Specify the type of DNS record to query (e.g., A, AAAA, MX, etc.).
- `-timeout=SECONDS`: Set the timeout for the query in seconds.
- `-retry=COUNT`: Set the number of retries for the query.
- `-debug`: Enable debugging mode for more detailed output.

## Common Examples
Here are some practical examples of using the `nslookup` command:

### Querying an A Record
To find the IP address associated with a domain name:

```bash
nslookup example.com
```

### Querying a Specific Record Type
To query for MX (Mail Exchange) records for a domain:

```bash
nslookup -type=MX example.com
```

### Specifying a DNS Server
To query a specific DNS server instead of the default:

```bash
nslookup example.com 8.8.8.8
```

### Debugging a Query
To enable debugging and get more detailed information about the DNS query process:

```bash
nslookup -debug example.com
```

## Tips
- Use `nslookup` to quickly verify if a domain is resolving correctly.
- When troubleshooting, try querying different DNS servers to see if the issue is server-specific.
- Familiarize yourself with different record types (A, AAAA, CNAME, MX, etc.) to make the most of `nslookup`.