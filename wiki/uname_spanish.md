# [Debian] Debian Almquist Shell (dash) uname Uso: Muestra información del sistema

## Overview
El comando `uname` se utiliza para mostrar información sobre el sistema operativo en el que se está ejecutando. Proporciona detalles como el nombre del kernel, la versión, el tipo de máquina y más.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
uname [options] [arguments]
```

## Common Options
- `-a`: Muestra toda la información disponible.
- `-s`: Muestra el nombre del kernel.
- `-n`: Muestra el nombre del nodo de red.
- `-r`: Muestra la versión del kernel.
- `-v`: Muestra la fecha de compilación del kernel.
- `-m`: Muestra el tipo de máquina.
- `-p`: Muestra el tipo de procesador (puede no estar disponible en todos los sistemas).
- `-i`: Muestra la plataforma de hardware.
- `-o`: Muestra el nombre del sistema operativo.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `uname`:

1. Mostrar toda la información del sistema:
   ```bash
   uname -a
   ```

2. Mostrar solo el nombre del kernel:
   ```bash
   uname -s
   ```

3. Mostrar la versión del kernel:
   ```bash
   uname -r
   ```

4. Mostrar el tipo de máquina:
   ```bash
   uname -m
   ```

5. Mostrar el nombre del nodo de red:
   ```bash
   uname -n
   ```

## Tips
- Utiliza `uname -a` para obtener un resumen completo de la información del sistema en un solo comando.
- Si solo necesitas información específica, usa las opciones individuales para simplificar la salida.
- Recuerda que algunos sistemas pueden no soportar todas las opciones, así que verifica la documentación de tu sistema si encuentras algún problema.