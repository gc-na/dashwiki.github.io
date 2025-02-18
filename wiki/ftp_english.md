# [English] Debian Almquist Shell (dash) ftp usage: Transfer files over a network

## Overview
The `ftp` command in the Debian Almquist Shell (dash) is used for transferring files between a local computer and a remote server using the File Transfer Protocol (FTP). It allows users to upload and download files, manage directories, and perform various file operations on the remote server.

## Usage
The basic syntax of the `ftp` command is as follows:

```bash
ftp [options] [arguments]
```

## Common Options
- `-i`: Turns off interactive prompting during multiple file transfers.
- `-v`: Enables verbose mode, providing detailed information about the transfer process.
- `-n`: Restricts auto-login upon initial connection.
- `-p`: Enables passive mode, which can help with firewalls and NAT.

## Common Examples

### Connecting to a Remote FTP Server
To connect to an FTP server, use the following command:

```bash
ftp ftp.example.com
```

### Uploading a File
To upload a file from your local machine to the remote server, use the `put` command after connecting:

```bash
put localfile.txt
```

### Downloading a File
To download a file from the remote server to your local machine, use the `get` command:

```bash
get remotefile.txt
```

### Listing Files in a Directory
To list files in the current directory on the remote server, use:

```bash
ls
```

### Changing Directories
To change to a different directory on the remote server, use the `cd` command:

```bash
cd /path/to/directory
```

## Tips
- Always use `bye` or `quit` to properly close the FTP session.
- Consider using `-p` for passive mode if you encounter connection issues behind a firewall.
- Use `-i` when transferring multiple files to avoid confirmation prompts for each file.