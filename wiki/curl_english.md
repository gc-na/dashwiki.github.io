# [English] Debian Almquist Shell (dash) curl usage: Transfer data from or to a server

## Overview
The `curl` command is a versatile tool used to transfer data to or from a server using various protocols, including HTTP, HTTPS, FTP, and more. It is widely used for downloading files, interacting with APIs, and testing network connections.

## Usage
The basic syntax of the `curl` command is as follows:

```bash
curl [options] [arguments]
```

## Common Options
Here are some commonly used options with `curl`:

- `-O`: Save the output to a file named after the remote file.
- `-L`: Follow redirects.
- `-d`: Send data in a POST request.
- `-H`: Include custom headers in the request.
- `-u`: Provide user credentials for authentication.
- `-I`: Fetch the HTTP headers only.

## Common Examples

1. **Download a file:**
   To download a file from a URL and save it with the same name:
   ```bash
   curl -O http://example.com/file.txt
   ```

2. **Follow redirects:**
   To download a file while following any redirects:
   ```bash
   curl -LO http://example.com/redirected-file.txt
   ```

3. **Send a POST request:**
   To send data to a server using a POST request:
   ```bash
   curl -d "param1=value1&param2=value2" http://example.com/api
   ```

4. **Include custom headers:**
   To include a custom header in your request:
   ```bash
   curl -H "Authorization: Bearer token" http://example.com/api
   ```

5. **Fetch HTTP headers only:**
   To retrieve only the HTTP headers from a URL:
   ```bash
   curl -I http://example.com
   ```

## Tips
- Always check the response code when using `curl` to ensure your request was successful.
- Use the `-v` option for verbose output to debug issues with your requests.
- Combine options for more complex requests, such as sending data with headers.
- Consider using `-o filename` to specify a custom output file name when downloading files.