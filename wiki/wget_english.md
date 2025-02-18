# [English] Debian Almquist Shell (dash) wget Usage: Download files from the web

## Overview
The `wget` command is a powerful utility used to download files from the web. It supports various protocols, including HTTP, HTTPS, and FTP, making it a versatile tool for retrieving content from the internet.

## Usage
The basic syntax of the `wget` command is as follows:

```bash
wget [options] [arguments]
```

## Common Options
Here are some common options you can use with `wget`:

- `-O <file>`: Save the downloaded file with a specific name.
- `-q`: Operate in quiet mode, suppressing output.
- `-c`: Resume a partially downloaded file.
- `--limit-rate=<rate>`: Limit the download speed to a specified rate.
- `-r`: Download files recursively.

## Common Examples

1. **Download a single file:**
   ```bash
   wget http://example.com/file.zip
   ```

2. **Download a file and save it with a specific name:**
   ```bash
   wget -O myfile.zip http://example.com/file.zip
   ```

3. **Resume a partially downloaded file:**
   ```bash
   wget -c http://example.com/largefile.zip
   ```

4. **Download a website recursively:**
   ```bash
   wget -r http://example.com
   ```

5. **Limit the download speed:**
   ```bash
   wget --limit-rate=200k http://example.com/largefile.zip
   ```

## Tips
- Use the `-q` option for scripts to avoid cluttering the output.
- Combine options for more complex downloads, such as `wget -c -O myfile.zip http://example.com/file.zip`.
- Check the `wget` manual (`man wget`) for more advanced features and options.