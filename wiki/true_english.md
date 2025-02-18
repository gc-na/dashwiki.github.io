# [English] Debian Almquist Shell (dash) true: Always succeed

## Overview
The `true` command in the Debian Almquist Shell (dash) is a simple utility that does nothing and always returns a successful exit status (0). It is often used in scripts and command lines where a command is required syntactically, but no action is needed.

## Usage
The basic syntax of the `true` command is as follows:

```bash
true [options] [arguments]
```

However, `true` does not take any options or arguments, and simply executes without performing any operations.

## Common Options
The `true` command does not have any options, as its sole purpose is to return a successful exit status.

## Common Examples

### Example 1: Basic Usage
You can run `true` directly in the terminal:

```bash
true
```

This command will execute and return an exit status of 0, indicating success.

### Example 2: Using true in a Conditional Statement
You can use `true` in a conditional statement within a shell script:

```bash
if true; then
    echo "This will always be printed."
fi
```

In this example, the message will always be printed because `true` always succeeds.

### Example 3: Looping with true
You can create an infinite loop using `true`:

```bash
while true; do
    echo "This will print indefinitely."
done
```

This command will continuously print the message until interrupted.

### Example 4: Placeholder in Scripts
`true` can be used as a placeholder in scripts where a command is required but no action is needed:

```bash
for i in 1 2 3; do
    true  # Placeholder for future commands
done
```

In this case, `true` serves as a placeholder for where you might later add functionality.

## Tips
- Use `true` in scripts to create placeholders for future commands or to maintain syntax without performing actions.
- It can be useful in testing scenarios where you want to simulate success without executing any real commands.
- Combine `true` with other commands in conditional statements to control the flow of your scripts effectively.