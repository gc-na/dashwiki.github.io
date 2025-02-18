# [Español] Debian Almquist Shell (dash) sort uso equivalente: ordenar líneas de texto

## Overview
El comando `sort` en el shell Almquist de Debian (dash) se utiliza para ordenar líneas de texto en archivos o en la entrada estándar. Es una herramienta útil para organizar datos y facilitar su análisis.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
sort [opciones] [argumentos]
```

## Common Options
- `-r`: Ordena las líneas en orden inverso.
- `-n`: Ordena numéricamente en lugar de alfabéticamente.
- `-k`: Especifica una clave de ordenación, permitiendo ordenar por columnas específicas.
- `-u`: Elimina líneas duplicadas en la salida.
- `-o`: Especifica un archivo de salida para guardar el resultado.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `sort`:

1. **Ordenar un archivo de texto alfabéticamente**:
   ```bash
   sort archivo.txt
   ```

2. **Ordenar un archivo numéricamente**:
   ```bash
   sort -n numeros.txt
   ```

3. **Ordenar en orden inverso**:
   ```bash
   sort -r archivo.txt
   ```

4. **Ordenar por una columna específica**:
   ```bash
   sort -k 2 archivo.txt
   ```

5. **Eliminar duplicados y ordenar**:
   ```bash
   sort -u archivo.txt
   ```

6. **Guardar la salida ordenada en un nuevo archivo**:
   ```bash
   sort archivo.txt -o archivo_ordenado.txt
   ```

## Tips
- Siempre verifica el contenido del archivo original antes de usar la opción `-o`, para evitar sobrescribir datos importantes.
- Usa `-k` para ordenar por columnas específicas, especialmente útil en archivos CSV o tabulados.
- Combina `sort` con otros comandos como `uniq` para un análisis más profundo de los datos.