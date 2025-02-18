# [Debian] Debian Almquist Shell (dash) uniq Uso: Eliminar líneas duplicadas en un archivo

## Overview
El comando `uniq` se utiliza para filtrar líneas duplicadas en un archivo o en la entrada estándar. Este comando es útil para procesar datos y obtener una lista de elementos únicos.

## Usage
La sintaxis básica del comando `uniq` es la siguiente:

```bash
uniq [opciones] [archivo]
```

## Common Options
- `-c`: Cuenta el número de ocurrencias de cada línea.
- `-d`: Muestra solo las líneas que están duplicadas.
- `-u`: Muestra solo las líneas que son únicas.
- `-i`: Ignora diferencias entre mayúsculas y minúsculas al comparar líneas.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `uniq`:

1. **Eliminar duplicados de un archivo:**
   ```bash
   uniq archivo.txt
   ```

2. **Contar ocurrencias de cada línea:**
   ```bash
   uniq -c archivo.txt
   ```

3. **Mostrar solo líneas duplicadas:**
   ```bash
   uniq -d archivo.txt
   ```

4. **Mostrar solo líneas únicas:**
   ```bash
   uniq -u archivo.txt
   ```

5. **Ignorar mayúsculas y minúsculas:**
   ```bash
   uniq -i archivo.txt
   ```

## Tips
- Asegúrate de que el archivo de entrada esté ordenado antes de usar `uniq`, ya que solo elimina duplicados consecutivos.
- Puedes combinar `uniq` con otros comandos como `sort` para obtener resultados más precisos. Por ejemplo:
  ```bash
  sort archivo.txt | uniq
  ```
- Utiliza la opción `-c` para obtener un resumen de cuántas veces aparece cada línea, lo que puede ser útil para análisis de datos.