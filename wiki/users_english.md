# [English] Debian Almquist Shell (dash) users usage: List logged-in users

## Overview
The `users` command in the Debian Almquist Shell (dash) is used to display the usernames of users currently logged into the system. It provides a simple way to see who is actively using the machine at any given time.

## Usage
The basic syntax of the `users` command is as follows:

```bash
users [options] [arguments]
```

## Common Options
The `users` command has a few common options, although it typically operates without any:

- `-n`: Suppresses the output of the user count.
- `-r`: Displays the usernames in reverse order.

## Common Examples

1. **Display currently logged-in users:**
   ```bash
   users
   ```

2. **Display logged-in users in reverse order:**
   ```bash
   users -r
   ```

3. **Suppress output of user count (if applicable):**
   ```bash
   users -n
   ```

## Tips
- The `users` command is often used in scripts to check user activity on a system.
- Combine `users` with other commands like `wc -w` to count the number of logged-in users:
  ```bash
  users | wc -w
  ```
- Remember that `users` only shows users who are currently logged in; it does not provide information about users who have logged out or are inactive.