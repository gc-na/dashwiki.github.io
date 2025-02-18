# [Debian] Debian Almquist Shell (dash) diff: Comparar archivos de texto

## Overview
El comando `diff` se utiliza para comparar el contenido de dos archivos de texto línea por línea. Muestra las diferencias entre ellos, lo que es útil para identificar cambios, errores o para fusionar archivos.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
diff [opciones] [archivo1] [archivo2]
```

## Common Options
- `-u`: Muestra las diferencias en un formato unificado, que es más fácil de leer.
- `-c`: Muestra las diferencias en un formato de contexto, que incluye algunas líneas de contexto alrededor de las diferencias.
- `-i`: Ignora diferencias en mayúsculas y minúsculas.
- `-w`: Ignora espacios en blanco al comparar.
- `-r`: Compara directorios de forma recursiva.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `diff`:

1. Comparar dos archivos de texto simples:
   ```bash
   diff archivo1.txt archivo2.txt
   ```

2. Mostrar las diferencias en formato unificado:
   ```bash
   diff -u archivo1.txt archivo2.txt
   ```

3. Ignorar diferencias en mayúsculas y minúsculas:
   ```bash
   diff -i archivo1.txt archivo2.txt
   ```

4. Comparar dos directorios recursivamente:
   ```bash
   diff -r directorio1/ directorio2/
   ```

5. Usar el formato de contexto para ver más líneas alrededor de las diferencias:
   ```bash
   diff -c archivo1.txt archivo2.txt
   ```

## Tips
- Utiliza la opción `-u` para obtener un formato más legible, especialmente si planeas enviar las diferencias a otros.
- Si estás trabajando con archivos de configuración, considera hacer copias de seguridad antes de aplicar cambios basados en las diferencias.
- Para una comparación más visual, puedes combinar `diff` con herramientas como `vimdiff` para ver las diferencias en un editor de texto.