# [English] Debian Almquist Shell (dash) shift Usage: Shift positional parameters

## Overview
The `shift` command in the Debian Almquist Shell (dash) is used to manipulate positional parameters in a shell script. It shifts the positional parameters to the left, effectively discarding the first parameter and moving all others one position down. This is particularly useful when processing command-line arguments in scripts.

## Usage
The basic syntax of the `shift` command is as follows:

```sh
shift [n]
```

Where `n` is an optional argument that specifies how many positions to shift. If `n` is not provided, it defaults to 1.

## Common Options
- `n`: An optional integer that specifies the number of positions to shift. If omitted, it defaults to 1.

## Common Examples

### Example 1: Basic Shift
This example demonstrates a simple shift of the positional parameters.

```sh
#!/bin/dash
set -- one two three four
echo "Before shift: $1 $2 $3 $4"
shift
echo "After shift: $1 $2 $3 $4"
```
**Output:**
```
Before shift: one two three four
After shift: two three four
```

### Example 2: Shift by Multiple Positions
You can shift multiple positions by specifying a number.

```sh
#!/bin/dash
set -- apple banana cherry date
echo "Before shift: $1 $2 $3 $4"
shift 2
echo "After shift: $1 $2 $3 $4"
```
**Output:**
```
Before shift: apple banana cherry date
After shift: cherry date
```

### Example 3: Using Shift in a Loop
This example shows how to use `shift` in a loop to process all positional parameters.

```sh
#!/bin/dash
set -- param1 param2 param3 param4
while [ "$#" -gt 0 ]; do
    echo "Current parameter: $1"
    shift
done
```
**Output:**
```
Current parameter: param1
Current parameter: param2
Current parameter: param3
Current parameter: param4
```

## Tips
- Use `shift` when you need to process command-line arguments one at a time in a loop.
- Remember that `shift` modifies the positional parameters, so be cautious if you need to access the original parameters later in your script.
- You can combine `shift` with other commands to create more complex argument parsing logic in your scripts.