# [Español] Debian Almquist Shell (dash) basename Uso equivalente en español: [extraer el nombre de un archivo]

## Overview
El comando `basename` se utiliza para extraer el nombre de un archivo de una ruta completa, eliminando cualquier prefijo de directorio. Esto es útil cuando se desea trabajar solo con el nombre del archivo sin la información de la ruta.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
basename [opciones] [argumentos]
```

## Common Options
- `-a`: Procesa todos los argumentos y devuelve el nombre base de cada uno.
- `-s`: Permite especificar una cadena que se eliminará del final del nombre del archivo.
- `--help`: Muestra la ayuda sobre el uso del comando.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `basename`:

1. Extraer el nombre de un archivo de una ruta completa:
   ```bash
   basename /ruta/al/archivo.txt
   ```
   Salida:
   ```
   archivo.txt
   ```

2. Eliminar una extensión de archivo:
   ```bash
   basename /ruta/al/archivo.txt .txt
   ```
   Salida:
   ```
   archivo
   ```

3. Procesar múltiples archivos a la vez:
   ```bash
   basename -a /ruta/al/archivo1.txt /ruta/al/archivo2.txt
   ```
   Salida:
   ```
   archivo1.txt
   archivo2.txt
   ```

4. Eliminar una cadena específica del final del nombre del archivo:
   ```bash
   basename /ruta/al/archivo_backup.txt -s _backup
   ```
   Salida:
   ```
   archivo
   ```

## Tips
- Utiliza `basename` en scripts para simplificar el manejo de nombres de archivos.
- Combinado con otros comandos como `find`, `basename` puede ser muy poderoso para procesar listas de archivos.
- Recuerda que `basename` solo elimina la ruta y no modifica el archivo original.