# [English] Debian Almquist Shell (dash) scp usage: Securely copy files between hosts

## Overview
The `scp` (secure copy) command is used to securely transfer files and directories between two hosts over a network. It leverages SSH (Secure Shell) for data transfer, ensuring that the data is encrypted during transit.

## Usage
The basic syntax of the `scp` command is as follows:

```bash
scp [options] [source] [destination]
```

## Common Options
- `-r`: Recursively copy entire directories.
- `-P port`: Specify the port to connect to on the remote host (note the uppercase 'P').
- `-i identity_file`: Use a specific private key for authentication.
- `-v`: Enable verbose mode for debugging purposes.
- `-C`: Enable compression during transfer to speed up the process.

## Common Examples
Here are some practical examples of using the `scp` command:

1. **Copy a file from local to remote:**
   ```bash
   scp /path/to/local/file.txt user@remote_host:/path/to/remote/directory/
   ```

2. **Copy a file from remote to local:**
   ```bash
   scp user@remote_host:/path/to/remote/file.txt /path/to/local/directory/
   ```

3. **Copy a directory recursively from local to remote:**
   ```bash
   scp -r /path/to/local/directory user@remote_host:/path/to/remote/
   ```

4. **Copy a file using a specific port:**
   ```bash
   scp -P 2222 /path/to/local/file.txt user@remote_host:/path/to/remote/
   ```

5. **Copy a file using a specific identity file:**
   ```bash
   scp -i /path/to/private_key.pem /path/to/local/file.txt user@remote_host:/path/to/remote/
   ```

## Tips
- Always ensure that the SSH service is running on the remote host before attempting to use `scp`.
- Use the `-v` option for troubleshooting if you encounter issues during the transfer.
- Consider using `-C` for larger files to reduce transfer time by enabling compression.
- Be cautious with permissions and ownership when copying files to ensure they are set correctly on the destination.