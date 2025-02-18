# [Español] Debian Almquist Shell (dash) getopts uso: [analizar opciones de línea de comandos]

## Overview
El comando `getopts` se utiliza en scripts de shell para analizar opciones y argumentos de línea de comandos. Permite a los usuarios definir opciones que pueden ser pasadas al script, facilitando la gestión de argumentos.

## Usage
La sintaxis básica del comando `getopts` es la siguiente:

```sh
getopts [options] [arguments]
```

## Common Options
- `-a`: Permite que `getopts` acepte opciones de múltiples caracteres.
- `-o`: Especifica las opciones que se pueden pasar al script.
- `-l`: Permite el uso de opciones largas (no estándar en todas las implementaciones).

## Common Examples
### Ejemplo 1: Analizar opciones simples
```sh
#!/bin/sh
while getopts "ab:c" opt; do
  case $opt in
    a)
      echo "Opción a seleccionada"
      ;;
    b)
      echo "Opción b con argumento: $OPTARG"
      ;;
    c)
      echo "Opción c seleccionada"
      ;;
    *)
      echo "Opción no válida"
      ;;
  esac
done
```

### Ejemplo 2: Usar getopts en un script
```sh
#!/bin/sh
while getopts "f:o:" opt; do
  case $opt in
    f)
      echo "Archivo de entrada: $OPTARG"
      ;;
    o)
      echo "Archivo de salida: $OPTARG"
      ;;
    *)
      echo "Uso: $0 -f archivo_entrada -o archivo_salida"
      ;;
  esac
done
```

### Ejemplo 3: Manejo de opciones no válidas
```sh
#!/bin/sh
while getopts "x:y:z" opt; do
  case $opt in
    x)
      echo "Opción x: $OPTARG"
      ;;
    y)
      echo "Opción y: $OPTARG"
      ;;
    z)
      echo "Opción z seleccionada"
      ;;
    *)
      echo "Opción no válida: -$OPTARG"
      ;;
  esac
done
```

## Tips
- Siempre incluye un caso por defecto (`*`) en tu estructura `case` para manejar opciones no válidas.
- Utiliza `OPTARG` para acceder al argumento asociado con una opción que requiere un valor.
- Recuerda que `getopts` solo maneja opciones que comienzan con un guion (`-`), así que asegúrate de que tus argumentos sigan este formato.