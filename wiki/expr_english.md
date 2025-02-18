# [English] Debian Almquist Shell (dash) expr Usage equivalent in English: Evaluate expressions

## Overview
The `expr` command in the Debian Almquist Shell (dash) is used to evaluate expressions and perform arithmetic operations, string manipulations, and comparisons. It is a simple yet powerful tool for scripting and command-line operations.

## Usage
The basic syntax of the `expr` command is as follows:

```sh
expr [options] [arguments]
```

## Common Options
- `+` : Addition operator.
- `-` : Subtraction operator.
- `*` : Multiplication operator (must be escaped as `\*`).
- `/` : Division operator.
- `%` : Modulus operator.
- `=` : Equality comparison.
- `!=` : Inequality comparison.
- `>` : Greater than comparison.
- `<` : Less than comparison.
- `length` : Returns the length of a string.

## Common Examples
Here are some practical examples of using the `expr` command:

### Arithmetic Operations
```sh
expr 5 + 3
```
This evaluates to `8`.

```sh
expr 10 \* 2
```
This evaluates to `20`. Note that the `*` operator must be escaped.

### String Length
```sh
expr length "Hello, World!"
```
This returns `13`, which is the length of the string.

### String Comparison
```sh
expr "apple" = "apple"
```
This evaluates to `1`, indicating that the strings are equal.

```sh
expr "apple" != "orange"
```
This evaluates to `1`, indicating that the strings are not equal.

### Conditional Evaluation
```sh
expr 5 \> 3
```
This evaluates to `1`, meaning true, as 5 is greater than 3.

## Tips
- Always escape the `*` operator with a backslash to avoid shell expansion.
- Use parentheses to group expressions for clarity, e.g., `expr \( 5 + 3 \) \* 2`.
- Be cautious with string comparisons; ensure the strings are quoted to avoid unexpected behavior.