# [English] Debian Almquist Shell (dash) tr <Usage equivalent in English>: Translate or delete characters

## Overview
The `tr` command in the Debian Almquist Shell (dash) is used to translate or delete characters from standard input. It reads input from a file or standard input, processes it according to the specified rules, and outputs the result.

## Usage
The basic syntax of the `tr` command is as follows:

```bash
tr [options] [arguments]
```

## Common Options
- `-d`: Delete characters specified in the arguments.
- `-s`: Squeeze multiple adjacent occurrences of a character into a single occurrence.
- `-c`: Complement the set of characters specified in the arguments.

## Common Examples

1. **Translate lowercase to uppercase:**
   ```bash
   echo "hello world" | tr 'a-z' 'A-Z'
   ```
   This command converts all lowercase letters in the input to uppercase.

2. **Delete specific characters:**
   ```bash
   echo "hello world" | tr -d 'lo'
   ```
   This command removes all occurrences of the letters 'l' and 'o' from the input.

3. **Squeeze repeated characters:**
   ```bash
   echo "heeeellooo" | tr -s 'e' 'o'
   ```
   This command replaces multiple occurrences of 'e' with a single 'o'.

4. **Complement character set:**
   ```bash
   echo "hello 123" | tr -c '0-9' ' '
   ```
   This command replaces all non-numeric characters with spaces.

## Tips
- Always quote your character sets to avoid shell interpretation issues.
- Use `cat` with `tr` for processing files directly, like `cat file.txt | tr 'a' 'b'`.
- Combine `tr` with other commands using pipes for more complex processing tasks.