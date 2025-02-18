# [English] Debian Almquist Shell (dash) sftp Usage: Secure File Transfer Protocol Command

## Overview
The `sftp` command in the Debian Almquist Shell (dash) is used for secure file transfer over the SSH protocol. It allows users to transfer files to and from a remote server securely, making it a preferred choice for many when dealing with sensitive data.

## Usage
The basic syntax of the `sftp` command is as follows:

```bash
sftp [options] [user@]host
```

## Common Options
- `-o`: Specify options in the format used in the SSH command.
- `-P`: Specify the port to connect to on the remote host.
- `-b`: Use a batch file for non-interactive mode.
- `-v`: Enable verbose mode for debugging.

## Common Examples
Here are some practical examples of using the `sftp` command:

1. **Connecting to a remote server:**
   ```bash
   sftp user@hostname
   ```

2. **Transferring a file from local to remote:**
   ```bash
   sftp user@hostname:/path/to/remote/dir <<< $'put localfile.txt'
   ```

3. **Transferring a file from remote to local:**
   ```bash
   sftp user@hostname:/path/to/remote/file.txt <<< $'get file.txt'
   ```

4. **Using a specific port to connect:**
   ```bash
   sftp -P 2222 user@hostname
   ```

5. **Using a batch file for multiple commands:**
   ```bash
   sftp -b batchfile.txt user@hostname
   ```

## Tips
- Always ensure that your SSH keys are set up for passwordless authentication to streamline your file transfers.
- Use the `-v` option when troubleshooting connection issues to get detailed output.
- Regularly check the permissions of your files and directories on the remote server to maintain security.