# [Debian] Debian Almquist Shell (dash) w: Display who is logged on and what they are doing

## Overview
The `w` command in the Debian Almquist Shell (dash) is used to display information about users currently logged into the system and their activities. It provides a summary of user sessions, including their login time, idle time, and the command they are currently executing.

## Usage
The basic syntax of the `w` command is as follows:

```bash
w [options] [arguments]
```

## Common Options
- `-h`: Omit the header line from the output.
- `-s`: Display the output in a more compact format.
- `-u`: Show the user's idle time in a more human-readable format.

## Common Examples

1. **Basic Usage**
   To display a list of currently logged-in users and their activities:
   ```bash
   w
   ```

2. **Omitting the Header**
   To show the user activity without the header line:
   ```bash
   w -h
   ```

3. **Compact Format**
   To display the information in a more compact format:
   ```bash
   w -s
   ```

4. **Human-Readable Idle Time**
   To show the idle time in a more understandable format:
   ```bash
   w -u
   ```

5. **Combining Options**
   To display the output without the header and in a compact format:
   ```bash
   w -hs
   ```

## Tips
- Use `w` regularly to monitor user activity on a multi-user system.
- Combine options to customize the output to your needs, especially when dealing with many users.
- If you are troubleshooting performance issues, `w` can help identify users who are consuming system resources.