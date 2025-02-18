# [Español] Debian Almquist Shell (dash) sed Uso: Modificar texto en flujos de datos

## Overview
El comando `sed` (Stream Editor) se utiliza para realizar transformaciones básicas en un flujo de texto. Permite editar, buscar y reemplazar texto en archivos o en la entrada estándar de manera eficiente.

## Usage
La sintaxis básica del comando `sed` es la siguiente:

```bash
sed [opciones] [argumentos]
```

## Common Options
- `-e`: Permite especificar múltiples expresiones de edición.
- `-i`: Edita los archivos en su lugar (modifica el archivo original).
- `-n`: Suprime la salida automática, permitiendo mostrar solo las líneas especificadas.
- `s/patrón/reemplazo/`: Realiza una sustitución del patrón por el reemplazo en cada línea.

## Common Examples
1. **Reemplazar texto en un archivo:**
   ```bash
   sed 's/hola/adiós/' archivo.txt
   ```
   Este comando reemplaza la primera aparición de "hola" por "adiós" en cada línea de `archivo.txt`.

2. **Reemplazar todas las apariciones de un texto:**
   ```bash
   sed 's/hola/adiós/g' archivo.txt
   ```
   Aquí, el modificador `g` hace que se reemplacen todas las ocurrencias de "hola" por "adiós".

3. **Eliminar líneas que contienen un patrón:**
   ```bash
   sed '/patrón/d' archivo.txt
   ```
   Este comando elimina todas las líneas que contienen "patrón" en `archivo.txt`.

4. **Modificar el archivo original:**
   ```bash
   sed -i 's/hola/adiós/g' archivo.txt
   ```
   Utilizando la opción `-i`, este comando modifica directamente `archivo.txt`, reemplazando "hola" por "adiós".

5. **Mostrar solo líneas que coinciden con un patrón:**
   ```bash
   sed -n '/patrón/p' archivo.txt
   ```
   Con la opción `-n`, este comando solo muestra las líneas que contienen "patrón".

## Tips
- Siempre es recomendable hacer una copia de seguridad del archivo original antes de usar la opción `-i`.
- Puedes combinar múltiples comandos `sed` usando `-e` para realizar varias transformaciones en una sola ejecución.
- Para pruebas, puedes usar `sed` sin `-i` para ver los resultados antes de aplicar cambios permanentes.