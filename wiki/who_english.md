# [English] Debian Almquist Shell (dash) who: Display logged-in users

## Overview
The `who` command in the Debian Almquist Shell (dash) is used to display a list of users who are currently logged into the system. It provides information such as the username, terminal, login time, and originating IP address or hostname.

## Usage
The basic syntax of the `who` command is as follows:

```
who [options] [arguments]
```

## Common Options
- `-u`: Show users and their idle time.
- `-q`: Display only the usernames and the number of users logged in.
- `-H`: Print the column headers before the output.
- `-m`: Show information about the current terminal session.

## Common Examples

1. **Basic usage**: Display all logged-in users.
   ```bash
   who
   ```

2. **Show idle time**: Display users along with their idle time.
   ```bash
   who -u
   ```

3. **Quick summary**: Get a quick count of logged-in users.
   ```bash
   who -q
   ```

4. **Include headers**: Display logged-in users with headers.
   ```bash
   who -H
   ```

5. **Current session**: Show information about the current terminal session.
   ```bash
   who -m
   ```

## Tips
- Use `who -u` to quickly identify users who may not be actively using the system, which can help in managing resources.
- Combine `who` with other commands, like `grep`, to filter results based on specific criteria (e.g., usernames).
- Regularly check logged-in users, especially on multi-user systems, to monitor activity and ensure security.