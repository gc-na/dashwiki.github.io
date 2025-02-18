# [English] Debian Almquist Shell (dash) at: Schedule commands to run at a specified time

## Overview
The `at` command in the Debian Almquist Shell (dash) is used to schedule commands to be executed at a specific time in the future. This is particularly useful for automating tasks that need to run once at a designated time without requiring user intervention.

## Usage
The basic syntax for the `at` command is as follows:

```bash
at [options] [time]
```

## Common Options
- `-f FILE`: Read commands from the specified file instead of standard input.
- `-m`: Send mail to the user after the command has been executed, even if there was no output.
- `-q QUEUE`: Specify the queue to use for the job.
- `-V`: Print the version of `at` and exit.

## Common Examples

### Schedule a Command for Later
To schedule a command to run at a specific time, you can use:

```bash
echo "echo 'Hello, World!'" | at 15:00
```
This command will print "Hello, World!" at 3 PM.

### Schedule a Command for Tomorrow
To run a command tomorrow at a specific time, you can specify the date:

```bash
echo "backup.sh" | at 2:00 tomorrow
```
This will execute the `backup.sh` script at 2 AM the following day.

### Schedule a Command Using a Relative Time
You can also use relative time specifications:

```bash
echo "cleanup.sh" | at now + 1 hour
```
This will run the `cleanup.sh` script one hour from the current time.

### Read Commands from a File
If you have multiple commands to run, you can read them from a file:

```bash
at -f myscript.sh 17:00
```
This will execute all commands listed in `myscript.sh` at 5 PM.

## Tips
- Always check your scheduled jobs with the `atq` command to see what you have pending.
- Use `atrm JOB_ID` to remove a scheduled job if you change your mind.
- Consider using the `-m` option if you want to receive notifications after your commands run, especially for critical tasks.