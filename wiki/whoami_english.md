# [English] Debian Almquist Shell (dash) whoami Usage: Identify the current user

## Overview
The `whoami` command is a simple utility that displays the username of the current user logged into the terminal session. It is particularly useful for confirming your identity in multi-user environments or when running scripts.

## Usage
The basic syntax of the `whoami` command is as follows:

```bash
whoami [options] [arguments]
```

## Common Options
The `whoami` command has no specific options. It is a straightforward command that executes without additional parameters.

## Common Examples
Here are some practical examples of using the `whoami` command:

1. **Display the current user:**
   ```bash
   whoami
   ```
   This command will output the username of the user currently logged in.

2. **Using whoami in a script:**
   ```bash
   echo "Current user is: $(whoami)"
   ```
   This command will print a message along with the current user's name.

3. **Check user in a remote session:**
   If you are logged into a remote server via SSH, you can simply run:
   ```bash
   whoami
   ```
   This will show you the username you are using on that remote server.

## Tips
- Use `whoami` in scripts to verify the user context in which the script is running.
- Combine `whoami` with other commands to tailor outputs based on the current user.
- Remember that `whoami` will only return the username; it does not provide any other user-related information.