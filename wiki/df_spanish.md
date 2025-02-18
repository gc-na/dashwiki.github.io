# [Español] Debian Almquist Shell (dash) df Uso: Muestra el uso del espacio en disco

## Overview
El comando `df` se utiliza para mostrar la cantidad de espacio en disco utilizado y disponible en los sistemas de archivos montados. Es una herramienta útil para monitorear el uso del almacenamiento en tu sistema.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
df [opciones] [argumentos]
```

## Common Options
- `-h`: Muestra el tamaño en un formato legible para humanos (por ejemplo, en KB, MB, GB).
- `-T`: Muestra el tipo de sistema de archivos.
- `-a`: Incluye sistemas de archivos que tienen un tamaño de 0.
- `-i`: Muestra el uso de inodos en lugar del uso de espacio en disco.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `df`:

1. **Mostrar el uso del espacio en disco en formato legible:**

   ```bash
   df -h
   ```

2. **Mostrar el uso del espacio en disco junto con el tipo de sistema de archivos:**

   ```bash
   df -hT
   ```

3. **Incluir sistemas de archivos con tamaño 0:**

   ```bash
   df -a
   ```

4. **Mostrar el uso de inodos:**

   ```bash
   df -i
   ```

## Tips
- Utiliza la opción `-h` para facilitar la lectura de los resultados, especialmente en sistemas con grandes volúmenes de datos.
- Combina opciones, como `df -hT`, para obtener más información en un solo comando.
- Revisa regularmente el uso del espacio en disco para evitar problemas de almacenamiento en tu sistema.