# [English] Debian Almquist Shell (dash) umask Usage: Set default file permissions

## Overview
The `umask` command in the Debian Almquist Shell (dash) is used to set the default file permissions for newly created files and directories. It defines the permissions that will not be set when a new file or directory is created, effectively controlling the default access rights.

## Usage
The basic syntax of the `umask` command is as follows:

```bash
umask [options] [arguments]
```

## Common Options
- `-S`: Display the current umask in symbolic format.
- `-p`: Display the current umask value in a way that can be reused in a script.

## Common Examples

1. **Check Current Umask Value**
   To see the current umask value:
   ```bash
   umask
   ```

2. **Set Umask Value**
   To set the umask to `022`, which allows read and execute permissions for others but not write:
   ```bash
   umask 022
   ```

3. **Set Umask in Symbolic Format**
   To set the umask using symbolic notation, which removes write permissions for group and others:
   ```bash
   umask u=rwx,g=rx,o=rx
   ```

4. **Display Current Umask in Symbolic Format**
   To display the current umask in a more readable format:
   ```bash
   umask -S
   ```

5. **Persisting Umask Changes**
   To make the umask change permanent for a user, add the umask command to the user's shell profile file (e.g., `~/.profile`):
   ```bash
   echo 'umask 027' >> ~/.profile
   ```

## Tips
- Always check the current umask before creating files or directories to ensure they have the desired permissions.
- Use symbolic notation for easier readability when setting umask values.
- Remember that the umask value is subtracted from the default permissions; for example, a default permission of `666` for files minus a umask of `022` results in `644` permissions for new files.