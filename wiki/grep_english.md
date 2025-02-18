# [English] Debian Almquist Shell (dash) grep Usage equivalent in English: Search text using patterns

## Overview
The `grep` command is a powerful utility in the Debian Almquist Shell (dash) used for searching plain-text data for lines that match a specified pattern. It is commonly used to filter output or search through files for specific strings or regular expressions.

## Usage
The basic syntax of the `grep` command is as follows:

```bash
grep [options] [arguments]
```

## Common Options
- `-i`: Ignore case distinctions in both the pattern and the input files.
- `-v`: Invert the match, showing only lines that do not match the pattern.
- `-r`: Recursively search directories for the pattern.
- `-n`: Show line numbers along with matching lines.
- `-l`: Show only the names of files with matching lines, not the matching lines themselves.

## Common Examples
Here are some practical examples of using `grep`:

1. **Search for a specific word in a file:**
   ```bash
   grep "hello" myfile.txt
   ```

2. **Search for a word, ignoring case:**
   ```bash
   grep -i "hello" myfile.txt
   ```

3. **Search recursively in a directory:**
   ```bash
   grep -r "hello" /path/to/directory
   ```

4. **Show line numbers of matches:**
   ```bash
   grep -n "hello" myfile.txt
   ```

5. **Find files that do not contain a specific word:**
   ```bash
   grep -v "hello" myfile.txt
   ```

6. **List only the names of files containing a specific word:**
   ```bash
   grep -l "hello" *.txt
   ```

## Tips
- Use `grep` in combination with other commands using pipes to filter output effectively, e.g., `ps aux | grep "process_name"`.
- Regular expressions can enhance your search capabilities; consider using `-E` for extended regex support.
- To search for multiple patterns, you can use the `-e` option, like so: `grep -e "pattern1" -e "pattern2" myfile.txt`.