# [English] Debian Almquist Shell (dash) jobs usage equivalent in English: Manage background jobs

## Overview
The `jobs` command in the Debian Almquist Shell (dash) is used to display the status of jobs that are running in the background or have been stopped. It provides a way to manage and monitor these jobs, allowing users to see which processes are currently active in the shell session.

## Usage
The basic syntax of the `jobs` command is as follows:

```bash
jobs [options] [arguments]
```

## Common Options
- `-l`: Display the process ID (PID) of each job.
- `-n`: Show only jobs that have changed status since the last notification.
- `-p`: Print only the process IDs of the jobs.

## Common Examples

1. **List all background jobs:**
   To see all jobs running in the background, simply use:
   ```bash
   jobs
   ```

2. **List jobs with process IDs:**
   To include the process IDs in the output, use the `-l` option:
   ```bash
   jobs -l
   ```

3. **Show only jobs that have changed status:**
   If you want to see only the jobs that have changed since the last check, use the `-n` option:
   ```bash
   jobs -n
   ```

4. **Get process IDs of jobs:**
   To print only the process IDs of the jobs, use the `-p` option:
   ```bash
   jobs -p
   ```

## Tips
- Use `bg` to resume a stopped job in the background after checking its status with `jobs`.
- Combine `jobs` with `fg` to bring a background job to the foreground for interaction.
- Regularly check the status of your jobs to manage system resources effectively, especially when running multiple processes.