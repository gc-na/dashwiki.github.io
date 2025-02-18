# [Debian Almquist Shell (dash)] free comando: Muestra la memoria del sistema

## Overview
The `free` command is used to display the amount of free and used memory in the system. It provides a quick overview of memory usage, including physical memory, swap memory, and buffers/cache.

## Usage
The basic syntax of the `free` command is as follows:

```bash
free [options] [arguments]
```

## Common Options
- `-h`: Display the output in a human-readable format (e.g., KB, MB, GB).
- `-m`: Show memory usage in megabytes.
- `-g`: Show memory usage in gigabytes.
- `-s <seconds>`: Continuously display memory usage at specified intervals.
- `-t`: Display a total line showing the total amount of memory.

## Common Examples

1. **Basic Memory Usage**
   ```bash
   free
   ```

2. **Human-Readable Format**
   ```bash
   free -h
   ```

3. **Memory Usage in Megabytes**
   ```bash
   free -m
   ```

4. **Continuous Memory Monitoring**
   ```bash
   free -s 5
   ```

5. **Including Total Memory**
   ```bash
   free -t -h
   ```

## Tips
- Use the `-h` option for easier interpretation of memory values, especially on systems with large amounts of RAM.
- For monitoring memory usage over time, the `-s` option can be useful to see how memory usage changes.
- Combine `free` with other commands like `watch` to refresh the output at regular intervals, e.g., `watch free -h`.