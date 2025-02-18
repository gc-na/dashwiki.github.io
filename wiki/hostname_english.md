# [English] Debian Almquist Shell (dash) hostname usage: Display or set the system's hostname

## Overview
The `hostname` command in the Debian Almquist Shell (dash) is used to display or set the system's hostname. The hostname is a label that identifies a device on a network, making it easier to manage and communicate with other devices.

## Usage
The basic syntax of the `hostname` command is as follows:

```bash
hostname [options] [arguments]
```

## Common Options
- `-f`, `--fqdn`: Display the fully qualified domain name (FQDN) of the system.
- `-i`, `--ip-address`: Show the IP address associated with the hostname.
- `-s`, `--short`: Display the short hostname (the part before the first dot).
- `-V`, `--version`: Show the version of the hostname command.

## Common Examples
Here are some practical examples of using the `hostname` command:

1. Display the current hostname:
   ```bash
   hostname
   ```

2. Show the fully qualified domain name (FQDN):
   ```bash
   hostname -f
   ```

3. Display the short hostname:
   ```bash
   hostname -s
   ```

4. Show the IP address of the hostname:
   ```bash
   hostname -i
   ```

5. Set a new hostname (requires superuser privileges):
   ```bash
   sudo hostname new-hostname
   ```

## Tips
- Always check your current hostname before making changes to avoid confusion.
- Use the `-f` option to ensure you are aware of the full network identity of your machine.
- Remember that changing the hostname may require a restart of certain services or the system itself to take effect properly.