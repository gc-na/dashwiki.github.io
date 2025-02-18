# [Español] Debian Almquist Shell (dash) expr Uso equivalente: [evaluar expresiones]

## Overview
El comando `expr` se utiliza en la shell de Debian Almquist (dash) para evaluar expresiones aritméticas, lógicas y de cadena. Permite realizar cálculos simples y manipular cadenas de texto, lo que lo convierte en una herramienta útil para scripts y tareas de línea de comandos.

## Usage
La sintaxis básica del comando `expr` es la siguiente:

```bash
expr [opciones] [argumentos]
```

## Common Options
- `-e`: Permite evaluar expresiones aritméticas.
- `length`: Devuelve la longitud de una cadena.
- `index`: Devuelve la posición de la primera aparición de un carácter en una cadena.
- `substr`: Extrae una subcadena de una cadena dada.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `expr`:

### Ejemplo 1: Sumar dos números
```bash
expr 5 + 3
```
Salida:
```
8
```

### Ejemplo 2: Longitud de una cadena
```bash
expr length "Hola Mundo"
```
Salida:
```
10
```

### Ejemplo 3: Posición de un carácter en una cadena
```bash
expr index "Hola Mundo" "M"
```
Salida:
```
6
```

### Ejemplo 4: Extraer una subcadena
```bash
expr substr "Hola Mundo" 1 4
```
Salida:
```
Hola
```

## Tips
- Asegúrate de usar espacios alrededor de los operadores, ya que `expr` los requiere para funcionar correctamente.
- Para realizar operaciones aritméticas más complejas, considera usar `bc` o `awk`, que ofrecen más funcionalidades.
- Cuando trabajes con cadenas, ten en cuenta que `expr` es sensible a las mayúsculas y minúsculas.