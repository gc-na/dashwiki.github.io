# [Español] Debian Almquist Shell (dash) cd Uso: Cambiar de directorio

## Overview
El comando `cd` (cambiar directorio) se utiliza en la shell para navegar entre los diferentes directorios del sistema de archivos. Permite al usuario moverse a un directorio específico, facilitando el acceso a archivos y subdirectorios.

## Usage
La sintaxis básica del comando `cd` es la siguiente:

```bash
cd [opciones] [argumentos]
```

## Common Options
- `-`: Cambia al directorio anterior.
- `..`: Se mueve al directorio padre del directorio actual.
- `~`: Cambia al directorio home del usuario actual.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `cd`:

1. Cambiar al directorio home del usuario:
   ```bash
   cd ~
   ```

2. Volver al directorio anterior:
   ```bash
   cd -
   ```

3. Subir un nivel en la jerarquía de directorios:
   ```bash
   cd ..
   ```

4. Cambiar a un directorio específico:
   ```bash
   cd /ruta/al/directorio
   ```

5. Cambiar a un subdirectorio dentro del directorio actual:
   ```bash
   cd subdirectorio
   ```

## Tips
- Utiliza `cd -` para alternar rápidamente entre dos directorios.
- Puedes usar la tecla de tabulación para autocompletar nombres de directorios, lo que ahorra tiempo y evita errores tipográficos.
- Recuerda que las rutas pueden ser absolutas (comienzan desde la raíz del sistema) o relativas (basadas en el directorio actual).