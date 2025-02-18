# [Debian] Debian Almquist Shell (dash) gunzip uso: Descomprimir archivos .gz

## Overview
El comando `gunzip` se utiliza para descomprimir archivos que han sido comprimidos con el algoritmo gzip. Este comando es muy útil para manejar archivos de gran tamaño y reducir el espacio en disco.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
gunzip [opciones] [argumentos]
```

## Common Options
- `-c`: Descomprime el archivo y envía la salida a la salida estándar (stdout) en lugar de crear un archivo.
- `-f`: Fuerza la descompresión de archivos, incluso si el archivo de destino ya existe.
- `-k`: Mantiene el archivo original después de la descompresión.
- `-r`: Descomprime archivos de forma recursiva en directorios.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `gunzip`:

1. Descomprimir un archivo simple:
   ```bash
   gunzip archivo.gz
   ```

2. Descomprimir y mantener el archivo original:
   ```bash
   gunzip -k archivo.gz
   ```

3. Descomprimir un archivo y enviar la salida a la consola:
   ```bash
   gunzip -c archivo.gz
   ```

4. Descomprimir todos los archivos .gz en un directorio:
   ```bash
   gunzip *.gz
   ```

5. Descomprimir archivos de forma recursiva en un directorio:
   ```bash
   gunzip -r directorio/
   ```

## Tips
- Siempre verifica el espacio en disco antes de descomprimir archivos grandes para evitar problemas de almacenamiento.
- Utiliza la opción `-k` si deseas mantener una copia del archivo comprimido original.
- Para descomprimir archivos en un script, considera usar la opción `-c` y redirigir la salida a un archivo para evitar la pérdida de datos.