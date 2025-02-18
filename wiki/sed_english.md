# [English] Debian Almquist Shell (dash) sed Usage: Stream editor for filtering and transforming text

## Overview
The `sed` command, short for "stream editor," is a powerful tool used in the Debian Almquist Shell (dash) for parsing and transforming text. It reads input line by line, applies specified operations, and outputs the modified text. This makes it particularly useful for tasks such as text substitution, deletion, and insertion.

## Usage
The basic syntax of the `sed` command is as follows:

```bash
sed [options] [arguments]
```

## Common Options
- `-e`: Allows the execution of multiple editing commands.
- `-f`: Specifies a file containing `sed` commands to be executed.
- `-n`: Suppresses automatic printing of pattern space; use with `p` to print specific lines.
- `s`: Substitutes a specified string with another string.
- `d`: Deletes lines that match a specified pattern.

## Common Examples

### Example 1: Simple Substitution
Replace the first occurrence of "apple" with "orange" in a file.

```bash
sed 's/apple/orange/' filename.txt
```

### Example 2: Global Substitution
Replace all occurrences of "apple" with "orange" in a file.

```bash
sed 's/apple/orange/g' filename.txt
```

### Example 3: Deleting Lines
Delete all lines that contain the word "banana".

```bash
sed '/banana/d' filename.txt
```

### Example 4: Using -n Option
Print only lines that contain the word "fruit".

```bash
sed -n '/fruit/p' filename.txt
```

### Example 5: Using a Script File
Execute multiple `sed` commands stored in a file called `script.sed`.

```bash
sed -f script.sed filename.txt
```

## Tips
- Always test your `sed` commands on a backup of your file to avoid accidental data loss.
- Use the `-i` option for in-place editing if you want to modify the original file directly (e.g., `sed -i 's/apple/orange/g' filename.txt`).
- Combine `sed` with other commands using pipes for more complex text processing tasks.