# [Español] Debian Almquist Shell (dash) strace uso: Herramienta para rastrear llamadas al sistema

## Overview
El comando `strace` se utiliza para rastrear las llamadas al sistema y las señales que reciben los procesos en un sistema operativo. Es una herramienta muy útil para depurar programas y entender cómo interactúan con el sistema.

## Usage
La sintaxis básica del comando `strace` es la siguiente:

```bash
strace [opciones] [argumentos]
```

## Common Options
Aquí hay algunas opciones comunes que puedes usar con `strace`:

- `-c`: Resumen de estadísticas de llamadas al sistema.
- `-f`: Sigue los procesos hijos creados por el proceso rastreado.
- `-e expr`: Filtra las llamadas al sistema que se rastrean, donde `expr` puede ser un nombre de llamada o una expresión.
- `-o archivo`: Redirige la salida a un archivo en lugar de la salida estándar.
- `-p pid`: Adjunta a un proceso existente con el identificador de proceso `pid`.

## Common Examples
Aquí tienes algunos ejemplos prácticos del uso de `strace`:

1. Rastrear un comando simple:
   ```bash
   strace ls
   ```

2. Rastrear un proceso en ejecución:
   ```bash
   strace -p 1234
   ```

3. Guardar la salida en un archivo:
   ```bash
   strace -o salida.txt ls
   ```

4. Rastrear solo las llamadas de apertura de archivos:
   ```bash
   strace -e trace=open ls
   ```

5. Obtener un resumen de estadísticas de llamadas al sistema:
   ```bash
   strace -c ls
   ```

## Tips
- Utiliza `strace` con `-f` si el programa crea procesos hijos para asegurarte de rastrear todas las llamadas.
- Filtra las llamadas al sistema con `-e` para enfocarte en las que realmente te interesan.
- Revisa la salida de `strace` en un archivo para un análisis más detallado y evitar el desorden en la terminal.