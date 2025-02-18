# [Español] Debian Almquist Shell (dash) cmp Uso equivalente: Comparar archivos byte a byte

## Overview
El comando `cmp` se utiliza para comparar dos archivos byte a byte. Si los archivos son diferentes, `cmp` indica la primera posición donde difieren. Si son idénticos, no produce salida.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
cmp [opciones] [archivo1] [archivo2]
```

## Common Options
- `-l`: Muestra las diferencias en formato octal.
- `-s`: No muestra salida, solo devuelve el estado de comparación.
- `-i`: Ignora las diferencias en el número de bytes especificado.
- `--help`: Muestra la ayuda sobre el uso del comando.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `cmp`:

1. Comparar dos archivos y mostrar la primera diferencia:
   ```bash
   cmp archivo1.txt archivo2.txt
   ```

2. Comparar dos archivos sin mostrar salida, solo el estado:
   ```bash
   cmp -s archivo1.txt archivo2.txt
   ```

3. Comparar dos archivos y mostrar las diferencias en formato octal:
   ```bash
   cmp -l archivo1.txt archivo2.txt
   ```

4. Ignorar las diferencias en los primeros 10 bytes:
   ```bash
   cmp -i 10 archivo1.txt archivo2.txt
   ```

## Tips
- Utiliza `cmp -s` para verificar rápidamente si dos archivos son idénticos sin inundar la terminal con salida.
- Si necesitas ver las diferencias detalladas, `cmp -l` es muy útil para obtener información precisa.
- Recuerda que `cmp` es sensible a mayúsculas y minúsculas, así que ten cuidado al comparar archivos con nombres similares.