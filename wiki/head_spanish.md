# [Español] Debian Almquist Shell (dash) head uso equivalente: Muestra las primeras líneas de un archivo

## Overview
El comando `head` se utiliza para mostrar las primeras líneas de uno o más archivos de texto. Es especialmente útil para obtener una vista rápida del contenido sin necesidad de abrir el archivo completo.

## Usage
La sintaxis básica del comando es la siguiente:

```
head [opciones] [argumentos]
```

## Common Options
- `-n NUM`: Especifica el número de líneas que se mostrarán. Por defecto, se muestran las primeras 10 líneas.
- `-c NUM`: Muestra los primeros NUM bytes del archivo en lugar de líneas.
- `-q`: Suprime la impresión del encabezado de los archivos cuando se utilizan múltiples archivos.
- `-v`: Muestra el encabezado de los archivos, incluso si solo se especifica un archivo.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `head`:

1. Mostrar las primeras 10 líneas de un archivo:
   ```bash
   head archivo.txt
   ```

2. Mostrar las primeras 5 líneas de un archivo:
   ```bash
   head -n 5 archivo.txt
   ```

3. Mostrar los primeros 20 bytes de un archivo:
   ```bash
   head -c 20 archivo.txt
   ```

4. Mostrar las primeras 10 líneas de múltiples archivos:
   ```bash
   head archivo1.txt archivo2.txt
   ```

5. Suprimir el encabezado al mostrar múltiples archivos:
   ```bash
   head -q archivo1.txt archivo2.txt
   ```

## Tips
- Utiliza `head` en combinación con otros comandos, como `grep`, para filtrar resultados de manera más efectiva.
- Si deseas ver las primeras líneas de la salida de otro comando, puedes usar una tubería. Por ejemplo:
  ```bash
  ls -l | head -n 5
  ```
- Recuerda que `head` es útil para archivos grandes, ya que te permite obtener información sin cargar todo el archivo en memoria.