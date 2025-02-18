# [Debian] Debian Almquist Shell (dash) chmod uso: Cambiar permisos de archivos y directorios

## Overview
El comando `chmod` se utiliza para cambiar los permisos de acceso a archivos y directorios en sistemas Unix y Linux. Permite al usuario definir quién puede leer, escribir o ejecutar un archivo.

## Usage
La sintaxis básica del comando `chmod` es la siguiente:

```bash
chmod [opciones] [argumentos]
```

## Common Options
- `-R`: Aplica los cambios de forma recursiva a todos los archivos y subdirectorios dentro del directorio especificado.
- `-v`: Muestra información detallada sobre los cambios realizados.
- `-c`: Muestra información sobre los cambios solo si los permisos han cambiado.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `chmod`:

1. **Cambiar permisos de un archivo a solo lectura para el propietario:**
   ```bash
   chmod 400 archivo.txt
   ```

2. **Dar permisos de lectura y escritura al propietario, y solo lectura a los demás:**
   ```bash
   chmod 644 archivo.txt
   ```

3. **Hacer un script ejecutable:**
   ```bash
   chmod +x script.sh
   ```

4. **Cambiar permisos de un directorio y su contenido de forma recursiva:**
   ```bash
   chmod -R 755 /ruta/al/directorio
   ```

5. **Mostrar los cambios realizados al cambiar permisos:**
   ```bash
   chmod -v 600 archivo.txt
   ```

## Tips
- Siempre verifica los permisos actuales de un archivo usando `ls -l` antes de hacer cambios.
- Utiliza la opción `-R` con precaución, ya que puede cambiar los permisos de muchos archivos a la vez.
- Considera usar notación simbólica (como `u+x` para agregar permisos de ejecución al propietario) para cambios más específicos y legibles.