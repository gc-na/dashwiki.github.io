# [English] Debian Almquist Shell (dash) passwd Usage equivalent in English: Manage user passwords

## Overview
The `passwd` command in the Debian Almquist Shell (dash) is used to change user passwords. It allows users to update their own passwords or administrators to manage passwords for other users, enhancing system security.

## Usage
The basic syntax of the `passwd` command is as follows:

```bash
passwd [options] [username]
```

If no username is specified, it defaults to changing the password for the current user.

## Common Options
- `-d`: Delete the password for the specified user, allowing login without a password.
- `-l`: Lock the specified user's password, preventing login.
- `-u`: Unlock a previously locked user account.
- `-e`: Expire the user's password immediately, forcing a change at the next login.

## Common Examples

### Change Your Own Password
To change your own password, simply run:

```bash
passwd
```

### Change Another User's Password
If you are an administrator and want to change another user's password, use:

```bash
sudo passwd username
```

### Lock a User's Account
To lock a user account, preventing login, execute:

```bash
sudo passwd -l username
```

### Unlock a User's Account
To unlock a previously locked account, use:

```bash
sudo passwd -u username
```

### Delete a User's Password
To remove a password for a user, allowing login without a password, run:

```bash
sudo passwd -d username
```

### Expire a User's Password
To force a user to change their password at the next login, use:

```bash
sudo passwd -e username
```

## Tips
- Always ensure you have the necessary permissions to change another user's password.
- Use strong passwords to enhance security; consider using a password manager.
- Regularly update passwords to maintain system security and protect sensitive information.