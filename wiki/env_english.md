# [English] Debian Almquist Shell (dash) env usage: Manage environment variables

## Overview
The `env` command in the Debian Almquist Shell (dash) is used to run a command in a modified environment. It allows you to set or unset environment variables for the command that follows it, making it a useful tool for managing the execution context of scripts and commands.

## Usage
The basic syntax of the `env` command is as follows:

```sh
env [options] [arguments]
```

## Common Options
- `-i`: Start with an empty environment, ignoring the current environment variables.
- `-u NAME`: Remove the variable NAME from the environment.
- `-0`: Use a null character as the delimiter for the input arguments (useful for handling filenames with spaces).

## Common Examples

### 1. Running a command with a modified environment variable
You can use `env` to set a specific environment variable for a command:

```sh
env VAR_NAME=value command
```
Example:
```sh
env MY_VAR=Hello echo $MY_VAR
```
This will output nothing because `MY_VAR` is not set in the current shell.

### 2. Unsetting an environment variable
To run a command without a specific environment variable, you can use the `-u` option:

```sh
env -u VAR_NAME command
```
Example:
```sh
env -u MY_VAR echo $MY_VAR
```
This will also output nothing, as `MY_VAR` is removed from the environment.

### 3. Starting with an empty environment
To execute a command with no inherited environment variables, use the `-i` option:

```sh
env -i command
```
Example:
```sh
env -i bash -c 'echo $HOME'
```
This will not output anything, as the `HOME` variable is not set in the empty environment.

### 4. Running a command with multiple environment variables
You can set multiple variables at once:

```sh
env VAR1=value1 VAR2=value2 command
```
Example:
```sh
env VAR1=foo VAR2=bar printenv
```
This will output `VAR1=foo` and `VAR2=bar`, showing the variables set for the `printenv` command.

## Tips
- Use `env` to ensure that scripts run with the correct environment, especially when deploying applications.
- When debugging scripts, `env` can help isolate issues related to environment variables.
- Combine `env` with other commands in pipelines to manage environments flexibly.