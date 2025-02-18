# [English] Debian Almquist Shell (dash) test usage: Evaluate expressions

## Overview
The `test` command in the Debian Almquist Shell (dash) is used to evaluate conditional expressions. It allows users to check file types, compare strings, and evaluate numeric expressions, returning a success or failure status based on the evaluation.

## Usage
The basic syntax of the `test` command is as follows:

```sh
test [options] [arguments]
```

Alternatively, you can use the `[` command, which is a synonym for `test`:

```sh
[ [options] [arguments] ]
```

## Common Options
- `-e FILE`: Checks if the specified file exists.
- `-f FILE`: Checks if the specified file is a regular file.
- `-d FILE`: Checks if the specified file is a directory.
- `-r FILE`: Checks if the specified file is readable.
- `-w FILE`: Checks if the specified file is writable.
- `-x FILE`: Checks if the specified file is executable.
- `STRING1 = STRING2`: Checks if two strings are equal.
- `STRING1 != STRING2`: Checks if two strings are not equal.
- `NUM1 -eq NUM2`: Checks if two numbers are equal.
- `NUM1 -ne NUM2`: Checks if two numbers are not equal.

## Common Examples

### Check if a file exists
```sh
test -e myfile.txt && echo "File exists."
```

### Check if a directory exists
```sh
test -d /path/to/directory && echo "Directory exists."
```

### Compare two strings
```sh
test "hello" = "hello" && echo "Strings are equal."
```

### Check if a file is readable
```sh
test -r myfile.txt && echo "File is readable."
```

### Numeric comparison
```sh
num1=10
num2=20
test $num1 -lt $num2 && echo "$num1 is less than $num2."
```

## Tips
- Use the `[` command for better readability in scripts, as it visually indicates a conditional check.
- Always quote your string arguments to avoid issues with spaces or special characters.
- Combine multiple tests using logical operators like `&&` (and) and `||` (or) for more complex conditions.
- Remember that `test` returns a success status (0) for true conditions and a failure status (1) for false conditions, which can be useful in scripting.