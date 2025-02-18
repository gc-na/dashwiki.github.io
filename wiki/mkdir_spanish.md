# [Español] Debian Almquist Shell (dash) mkdir Uso: Crea directorios en el sistema de archivos

## Overview
El comando `mkdir` se utiliza para crear nuevos directorios en el sistema de archivos. Es una herramienta fundamental para organizar archivos y carpetas en un entorno Unix-like.

## Usage
La sintaxis básica del comando `mkdir` es la siguiente:

```bash
mkdir [opciones] [argumentos]
```

## Common Options
- `-p`: Crea directorios padres según sea necesario. Si los directorios intermedios no existen, los crea.
- `-m`: Establece los permisos del nuevo directorio utilizando un modo octal.
- `--help`: Muestra la ayuda sobre el uso del comando.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `mkdir`:

1. Crear un solo directorio:
   ```bash
   mkdir nuevo_directorio
   ```

2. Crear múltiples directorios a la vez:
   ```bash
   mkdir dir1 dir2 dir3
   ```

3. Crear un directorio y sus subdirectorios padres:
   ```bash
   mkdir -p padre/hijo/nieto
   ```

4. Crear un directorio con permisos específicos:
   ```bash
   mkdir -m 755 directorio_con_permisos
   ```

## Tips
- Siempre verifica si el directorio ya existe antes de intentar crearlo para evitar errores.
- Utiliza la opción `-p` para crear estructuras de directorios complejas sin preocuparte por la existencia de directorios intermedios.
- Considera establecer permisos adecuados al crear directorios, especialmente en entornos compartidos.