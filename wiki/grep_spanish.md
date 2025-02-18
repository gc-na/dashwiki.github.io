# [Español] Debian Almquist Shell (dash) grep Uso: Buscar texto en archivos

## Overview
El comando `grep` se utiliza para buscar patrones de texto dentro de archivos. Es una herramienta muy poderosa que permite filtrar y encontrar líneas que coinciden con una expresión regular específica.

## Usage
La sintaxis básica del comando `grep` es la siguiente:

```bash
grep [opciones] [patrón] [archivo]
```

## Common Options
- `-i`: Ignora la distinción entre mayúsculas y minúsculas.
- `-v`: Invertir la coincidencia; muestra las líneas que no coinciden con el patrón.
- `-r`: Busca recursivamente en todos los archivos dentro de un directorio.
- `-n`: Muestra el número de línea junto con las líneas coincidentes.
- `-l`: Muestra solo los nombres de los archivos que contienen el patrón.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `grep`:

1. Buscar una palabra en un archivo:
   ```bash
   grep "palabra" archivo.txt
   ```

2. Buscar sin distinguir entre mayúsculas y minúsculas:
   ```bash
   grep -i "palabra" archivo.txt
   ```

3. Buscar en todos los archivos de un directorio:
   ```bash
   grep "palabra" *
   ```

4. Mostrar el número de línea de las coincidencias:
   ```bash
   grep -n "palabra" archivo.txt
   ```

5. Buscar un patrón y mostrar solo los archivos que lo contienen:
   ```bash
   grep -l "palabra" *.txt
   ```

## Tips
- Usa `grep` junto con otros comandos mediante tuberías (`|`) para filtrar la salida de otros programas.
- Para patrones más complejos, considera usar expresiones regulares para mejorar la precisión de tu búsqueda.
- Recuerda que puedes combinar múltiples opciones para personalizar aún más tu búsqueda.