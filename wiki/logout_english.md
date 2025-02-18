# [English] Debian Almquist Shell (dash) logout Usage equivalent in English: Exit the current shell session

## Overview
The `logout` command in the Debian Almquist Shell (dash) is used to terminate the current shell session. It is primarily utilized in login shells, allowing users to exit their session cleanly.

## Usage
The basic syntax of the `logout` command is as follows:

```sh
logout [options]
```

## Common Options
The `logout` command does not have any specific options. It simply exits the current shell session when executed.

## Common Examples

1. **Exiting a login shell:**
   To exit a login shell, simply type:
   ```sh
   logout
   ```

2. **Using logout in a script:**
   If you have a script running in a login shell and want to exit after completing tasks, you can include:
   ```sh
   #!/bin/dash
   echo "Tasks completed."
   logout
   ```

3. **Exiting from a nested shell:**
   If you have opened a nested shell and want to exit back to the previous shell, you can use:
   ```sh
   exit
   ```
   However, if you are in a login shell, you should use `logout` to terminate the session completely.

## Tips
- Always ensure that you have saved your work before using `logout`, as it will close the session and any unsaved data may be lost.
- Use `exit` instead of `logout` if you are in a non-login shell; `exit` will terminate the current shell without affecting the overall session.
- If you are unsure whether you are in a login shell, you can check the shell prompt or use the command `echo $0` to see the shell type.