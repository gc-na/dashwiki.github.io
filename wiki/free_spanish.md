# [Debian] Debian Almquist Shell (dash) free: Muestra información sobre la memoria del sistema

## Overview
El comando `free` se utiliza para mostrar información sobre la memoria del sistema, incluyendo la memoria total, utilizada, libre y la memoria de intercambio (swap). Es una herramienta útil para monitorear el uso de la memoria en sistemas Linux.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
free [options]
```

## Common Options
- `-h`: Muestra la información en un formato legible para humanos (por ejemplo, en megabytes o gigabytes).
- `-m`: Muestra la información en megabytes.
- `-g`: Muestra la información en gigabytes.
- `-s <segundos>`: Actualiza la información cada <segundos> especificados.
- `-t`: Muestra un total de la memoria utilizada y libre.

## Common Examples

1. Mostrar la información de memoria en un formato legible para humanos:
   ```bash
   free -h
   ```

2. Mostrar la información de memoria en megabytes:
   ```bash
   free -m
   ```

3. Mostrar la información de memoria en gigabytes:
   ```bash
   free -g
   ```

4. Actualizar la información de memoria cada 5 segundos:
   ```bash
   free -s 5
   ```

5. Mostrar un total de la memoria utilizada y libre:
   ```bash
   free -t
   ```

## Tips
- Utiliza la opción `-h` para facilitar la lectura de la información sobre la memoria, especialmente en sistemas con grandes cantidades de RAM.
- Considera usar `free -s` en combinación con `watch` para monitorear el uso de memoria en tiempo real.
- Revisa la sección de memoria de intercambio (swap) para asegurarte de que tu sistema no esté utilizando demasiado, lo que podría afectar el rendimiento.