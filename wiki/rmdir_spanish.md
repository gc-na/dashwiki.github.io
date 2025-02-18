# [Español] Debian Almquist Shell (dash) rmdir Uso: Eliminar directorios vacíos

## Overview
El comando `rmdir` se utiliza para eliminar directorios vacíos en el sistema de archivos. Si el directorio contiene archivos o subdirectorios, el comando no podrá eliminarlo y mostrará un mensaje de error.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
rmdir [opciones] [argumentos]
```

## Common Options
- `--help`: Muestra la ayuda sobre el uso del comando.
- `--verbose`: Muestra información detallada sobre las acciones realizadas por el comando.

## Common Examples

1. **Eliminar un directorio vacío:**
   ```bash
   rmdir mi_directorio
   ```

2. **Eliminar varios directorios vacíos a la vez:**
   ```bash
   rmdir directorio1 directorio2 directorio3
   ```

3. **Mostrar ayuda sobre el comando:**
   ```bash
   rmdir --help
   ```

4. **Eliminar un directorio vacío y mostrar información detallada:**
   ```bash
   rmdir --verbose mi_directorio
   ```

## Tips
- Asegúrate de que el directorio esté vacío antes de intentar eliminarlo con `rmdir`.
- Utiliza `ls` para verificar el contenido del directorio antes de eliminarlo.
- Si necesitas eliminar un directorio que no está vacío, considera usar el comando `rm -r` en su lugar, pero ten cuidado, ya que eliminará todo el contenido del directorio.