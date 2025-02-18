# [English] Debian Almquist Shell (dash) renice usage: Adjust process priority

## Overview
The `renice` command in the Debian Almquist Shell (dash) is used to change the priority of running processes. By adjusting a process's priority, you can influence how much CPU time it receives relative to other processes. Lowering a process's priority allows other processes to run more smoothly, while increasing it can help ensure that a critical task gets the resources it needs.

## Usage
The basic syntax of the `renice` command is as follows:

```bash
renice [options] [arguments]
```

## Common Options
- `-n, --priority <priority>`: Specify the new priority value. The priority can range from -20 (highest priority) to 19 (lowest priority).
- `-p, --pid <pid>`: Change the priority of the process with the specified process ID (PID).
- `-u, --user <user>`: Change the priority of all processes owned by the specified user.

## Common Examples
Here are some practical examples of using the `renice` command:

1. **Change the priority of a specific process by PID:**
   ```bash
   renice -n 10 -p 1234
   ```
   This command sets the priority of the process with PID 1234 to 10.

2. **Increase the priority of a process:**
   ```bash
   renice -n -5 -p 5678
   ```
   This command raises the priority of the process with PID 5678 to -5.

3. **Change the priority of all processes owned by a user:**
   ```bash
   renice -n 15 -u username
   ```
   This command sets the priority of all processes owned by "username" to 15.

4. **Check the current priority of a process:**
   Although `renice` does not directly show current priorities, you can use the `ps` command:
   ```bash
   ps -o pid,ni,cmd -p 1234
   ```
   This command displays the PID, nice value (priority), and command of the process with PID 1234.

## Tips
- Always use caution when increasing the priority of processes, as it can lead to system instability if critical resources are monopolized.
- Use `renice` in conjunction with monitoring tools like `top` or `htop` to observe the effects of priority changes in real-time.
- Remember that only the superuser (root) can increase the priority of processes (set a negative nice value). Regular users can only lower the priority of their own processes.