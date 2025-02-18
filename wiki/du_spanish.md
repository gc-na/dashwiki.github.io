# [Español] Debian Almquist Shell (dash) du uso: Muestra el uso del disco

## Overview
El comando `du` (disk usage) se utiliza para estimar y mostrar el espacio en disco utilizado por archivos y directorios en un sistema de archivos. Es una herramienta útil para identificar qué archivos o carpetas están ocupando más espacio.

## Usage
La sintaxis básica del comando `du` es la siguiente:

```bash
du [opciones] [argumentos]
```

## Common Options
- `-h`: Muestra el tamaño en un formato legible por humanos (por ejemplo, KB, MB).
- `-s`: Muestra solo el total para cada argumento, sin listar los subdirectorios.
- `-a`: Muestra el tamaño de todos los archivos, no solo de los directorios.
- `-c`: Muestra un total acumulado al final de la salida.
- `--max-depth=N`: Limita la profundidad de la lista de directorios a N niveles.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `du`:

1. Mostrar el uso del disco de un directorio específico en un formato legible:
   ```bash
   du -h /ruta/al/directorio
   ```

2. Mostrar solo el total del uso del disco de un directorio:
   ```bash
   du -sh /ruta/al/directorio
   ```

3. Listar el uso del disco de todos los archivos y directorios en el directorio actual:
   ```bash
   du -ah
   ```

4. Mostrar el uso del disco con un total acumulado:
   ```bash
   du -ch /ruta/al/directorio/*
   ```

5. Limitar la salida a un nivel de profundidad específico:
   ```bash
   du --max-depth=1 -h /ruta/al/directorio
   ```

## Tips
- Utiliza la opción `-h` para facilitar la lectura de los tamaños, especialmente en directorios grandes.
- Combina `du` con `sort` para ordenar los resultados por tamaño:
  ```bash
  du -h /ruta/al/directorio | sort -h
  ```
- Si deseas encontrar rápidamente qué directorios están ocupando más espacio, usa `du -sh * | sort -h` en el directorio que deseas analizar.