# [English] Debian Almquist Shell (dash) getopts Usage: [parse command-line options]

## Overview
The `getopts` command in the Debian Almquist Shell (dash) is used to parse command-line options in shell scripts. It simplifies the process of handling options and arguments, allowing scripts to accept flags and parameters in a standardized way.

## Usage
The basic syntax of the `getopts` command is as follows:

```sh
getopts optstring variable
```

- `optstring`: A string that defines the valid options. Each option character can be followed by a colon (`:`) if it requires an argument.
- `variable`: The name of the variable that will store the option found.

## Common Options
- `-a`: This option is not standard for `getopts` but is often used in scripts for custom handling.
- `-b`: Similar to `-a`, this is not a standard option but can be defined in the `optstring`.
- `:`: Indicates that the option requires an argument.

## Common Examples

### Example 1: Basic Option Parsing
This example shows how to parse a single option `-a`.

```sh
#!/bin/sh
while getopts "a" opt; do
  case $opt in
    a)
      echo "Option -a was triggered."
      ;;
    \?)
      echo "Invalid option: -$OPTARG" >&2
      ;;
  esac
done
```

### Example 2: Options with Arguments
In this example, we parse the `-f` option which requires an argument.

```sh
#!/bin/sh
while getopts "f:" opt; do
  case $opt in
    f)
      echo "File name: $OPTARG"
      ;;
    \?)
      echo "Invalid option: -$OPTARG" >&2
      ;;
  esac
done
```

### Example 3: Multiple Options
This example demonstrates how to handle multiple options, both with and without arguments.

```sh
#!/bin/sh
while getopts "a:b:c" opt; do
  case $opt in
    a)
      echo "Option -a with argument: $OPTARG"
      ;;
    b)
      echo "Option -b with argument: $OPTARG"
      ;;
    c)
      echo "Option -c was triggered."
      ;;
    \?)
      echo "Invalid option: -$OPTARG" >&2
      ;;
  esac
done
```

## Tips
- Always include a case for `\?` to handle invalid options gracefully.
- Use `OPTIND` to reset the index of the next option to be processed if you need to call `getopts` multiple times in your script.
- Keep your `optstring` clear and concise to avoid confusion when adding new options.