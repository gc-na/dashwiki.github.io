# [English] Debian Almquist Shell (dash) id usage: Display user and group information

## Overview
The `id` command in the Debian Almquist Shell (dash) is used to display the user ID (UID) and group ID (GID) of the current user or a specified user. It provides information about the user's identity and the groups they belong to, which can be useful for permission and access control checks.

## Usage
The basic syntax of the `id` command is as follows:

```bash
id [options] [username]
```

## Common Options
- `-u`: Display only the effective user ID.
- `-g`: Display only the effective group ID.
- `-G`: Display all group IDs the user belongs to.
- `-n`: Display the name instead of the numeric ID.
- `-r`: Display the real ID instead of the effective ID.

## Common Examples

1. **Display current user information:**
   ```bash
   id
   ```

2. **Display user ID and group ID of a specific user:**
   ```bash
   id username
   ```

3. **Display only the effective user ID:**
   ```bash
   id -u
   ```

4. **Display only the effective group ID:**
   ```bash
   id -g
   ```

5. **Display all group IDs for the current user:**
   ```bash
   id -G
   ```

6. **Display the name of the current user instead of the numeric ID:**
   ```bash
   id -n
   ```

## Tips
- Use `id` without any options to quickly check your current user and group information.
- Combine options for more specific output, such as `id -Gn` to get a list of group names for the current user.
- When troubleshooting permission issues, use `id` to verify that your user is part of the necessary groups.