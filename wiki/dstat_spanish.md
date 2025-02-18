# [Debian] Debian Almquist Shell (dash) dstat Uso: Monitoreo de recursos del sistema

## Overview
El comando `dstat` es una herramienta de monitoreo en tiempo real que combina las funcionalidades de varios comandos como `vmstat`, `iostat`, `netstat`, y `ifstat`. Permite visualizar el uso de recursos del sistema, como CPU, memoria, disco y red, todo en un solo lugar.

## Usage
La sintaxis básica del comando `dstat` es la siguiente:

```bash
dstat [opciones] [argumentos]
```

## Common Options
- `-c`: Muestra el uso de la CPU.
- `-d`: Muestra la actividad de disco.
- `-n`: Muestra la actividad de red.
- `-m`: Muestra el uso de memoria.
- `--time`: Muestra la marca de tiempo en la salida.
- `-r`: Muestra la actividad de las páginas de memoria.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `dstat`:

1. **Monitorear el uso de CPU y disco:**
   ```bash
   dstat -c -d
   ```

2. **Monitorear la actividad de red y memoria:**
   ```bash
   dstat -n -m
   ```

3. **Monitorear todos los recursos con marcas de tiempo:**
   ```bash
   dstat --time -cdmn
   ```

4. **Monitorear la actividad de disco y red con intervalos de 2 segundos:**
   ```bash
   dstat -d -n 2
   ```

## Tips
- Utiliza `dstat` con opciones combinadas para obtener una visión más completa del rendimiento del sistema.
- Considera redirigir la salida a un archivo para un análisis posterior usando `dstat > salida.txt`.
- Si necesitas un monitoreo más prolongado, puedes usar `dstat` en combinación con `watch` para actualizar la salida en intervalos regulares.