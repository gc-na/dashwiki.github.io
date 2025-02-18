# [English] Debian Almquist Shell (dash) export Usage equivalent in English: Set environment variables

## Overview
The `export` command in the Debian Almquist Shell (dash) is used to set environment variables that can be accessed by child processes. When a variable is exported, it becomes part of the environment for any subsequently executed commands.

## Usage
The basic syntax of the `export` command is as follows:

```sh
export [options] [arguments]
```

## Common Options
- `-n`: Unsets the export attribute for the specified variable, making it no longer available to child processes.
- `-p`: Displays all exported variables and their values.

## Common Examples

### Example 1: Exporting a Variable
To export a variable named `MY_VAR` with the value `Hello World`, you can use:

```sh
MY_VAR="Hello World"
export MY_VAR
```

### Example 2: Exporting Multiple Variables
You can export multiple variables in a single command:

```sh
export VAR1="Value1" VAR2="Value2"
```

### Example 3: Unsetting an Exported Variable
To unset the export attribute of a variable, use the `-n` option:

```sh
export -n MY_VAR
```

### Example 4: Displaying Exported Variables
To display all currently exported variables, use the `-p` option:

```sh
export -p
```

## Tips
- Always ensure that the variable names you choose do not conflict with existing environment variables to avoid unexpected behavior.
- Use `export` before running scripts that rely on specific environment variables to ensure they are available.
- Remember that changes made to exported variables in a shell session will not persist after the session ends unless they are added to a startup file like `.bashrc` or `.profile`.