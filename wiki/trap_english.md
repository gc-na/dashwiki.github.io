# [English] Debian Almquist Shell (dash) trap Usage: Handle signals and cleanup

## Overview
The `trap` command in the Debian Almquist Shell (dash) is used to specify commands that will be executed when the shell receives certain signals or when a script exits. This is particularly useful for cleanup tasks, such as removing temporary files or restoring terminal settings.

## Usage
The basic syntax of the `trap` command is as follows:

```sh
trap [commands] [signals]
```

- `commands`: The commands to be executed when the specified signals are received.
- `signals`: The signals that will trigger the execution of the commands. This can include signals like `EXIT`, `INT`, `TERM`, etc.

## Common Options
- `EXIT`: This signal is triggered when the script exits, allowing for cleanup tasks.
- `INT`: This signal is triggered when the user interrupts the script (usually by pressing Ctrl+C).
- `TERM`: This signal is sent to terminate the script, allowing for graceful shutdown procedures.

## Common Examples

### Example 1: Cleanup on Exit
This example shows how to remove a temporary file when the script exits.

```sh
trap 'rm -f /tmp/mytempfile' EXIT
echo "Doing some work..."
# Simulate work
sleep 5
```

### Example 2: Handle Interrupt Signal
In this example, the script will display a message and exit gracefully when interrupted.

```sh
trap 'echo "Script interrupted!"; exit' INT
echo "Running script... (Press Ctrl+C to interrupt)"
# Simulate long-running process
sleep 10
```

### Example 3: Multiple Signals
You can specify multiple signals to trigger the same command. Here’s how to handle both `INT` and `TERM` signals.

```sh
trap 'echo "Received termination signal"; exit' INT TERM
echo "Running script... (Press Ctrl+C or send TERM signal)"
# Simulate long-running process
sleep 10
```

## Tips
- Always include cleanup commands with the `EXIT` signal to ensure resources are released properly.
- Use `trap` at the beginning of your script to set up signal handling before any long-running processes start.
- Test your scripts to ensure that the `trap` commands behave as expected under various signal conditions.