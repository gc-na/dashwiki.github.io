# [English] Debian Almquist Shell (dash) nohup Usage: Run commands immune to hangups

## Overview
The `nohup` command in the Debian Almquist Shell (dash) allows you to run a command that will continue executing even after you log out or close the terminal. This is particularly useful for long-running processes that you want to ensure complete without interruption.

## Usage
The basic syntax of the `nohup` command is as follows:

```bash
nohup [options] [arguments]
```

## Common Options
- `&`: Run the command in the background.
- `-h`: Display help information.
- `-p`: Ignore the SIGHUP signal for the command.

## Common Examples
Here are some practical examples of using `nohup`:

1. **Running a script in the background:**
   ```bash
   nohup ./my_script.sh &
   ```

2. **Running a command and redirecting output to a file:**
   ```bash
   nohup my_long_running_command > output.log &
   ```

3. **Running a Python script:**
   ```bash
   nohup python3 my_script.py &
   ```

4. **Running a command with both stdout and stderr redirected:**
   ```bash
   nohup my_command > output.log 2>&1 &
   ```

## Tips
- Always redirect output to a file when using `nohup`, as it will create a default `nohup.out` file in the current directory if no output redirection is specified.
- Use the `&` at the end of the command to ensure it runs in the background, allowing you to continue using the terminal.
- Check the output file for any errors or logs related to the command after it has finished executing.