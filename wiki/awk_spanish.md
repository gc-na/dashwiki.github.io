# [Español] Debian Almquist Shell (dash) awk Uso: Procesamiento de texto y análisis de datos

## Overview
El comando `awk` es una herramienta poderosa para el procesamiento de texto y análisis de datos en la línea de comandos. Permite realizar operaciones complejas en archivos de texto, como la búsqueda, la manipulación y el reporte de datos, todo ello de manera eficiente.

## Usage
La sintaxis básica del comando `awk` es la siguiente:

```bash
awk [opciones] [argumentos]
```

## Common Options
- `-F`: Establece el delimitador de campo. Por defecto, `awk` utiliza espacios o tabulaciones como delimitadores.
- `-v`: Permite definir variables antes de ejecutar el script `awk`.
- `-f`: Especifica un archivo que contiene el script `awk` a ejecutar.
- `-W`: Activa opciones específicas del sistema, como el manejo de advertencias.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `awk`:

1. **Imprimir la primera columna de un archivo:**
   ```bash
   awk '{print $1}' archivo.txt
   ```

2. **Usar un delimitador específico (coma) para imprimir la segunda columna:**
   ```bash
   awk -F',' '{print $2}' archivo.csv
   ```

3. **Contar el número de líneas en un archivo:**
   ```bash
   awk 'END {print NR}' archivo.txt
   ```

4. **Filtrar líneas donde el valor en la tercera columna es mayor que 100:**
   ```bash
   awk '$3 > 100' archivo.txt
   ```

5. **Sumar los valores de la segunda columna:**
   ```bash
   awk '{sum += $2} END {print sum}' archivo.txt
   ```

## Tips
- Utiliza `-F` para definir delimitadores personalizados cuando trabajes con archivos que no usan espacios.
- Aprovecha el uso de variables con `-v` para hacer que tus scripts sean más legibles y flexibles.
- Siempre verifica la salida de `awk` con un archivo de prueba antes de aplicarlo a datos importantes para evitar errores.