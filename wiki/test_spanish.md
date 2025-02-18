# [Español] Debian Almquist Shell (dash) test uso: Comprobar expresiones

## Overview
El comando `test` en el shell Almquist de Debian (dash) se utiliza para evaluar expresiones condicionales. Permite verificar condiciones como la existencia de archivos, comparaciones numéricas y de cadenas, entre otras. Es fundamental para la toma de decisiones en scripts de shell.

## Usage
La sintaxis básica del comando `test` es la siguiente:

```bash
test [opciones] [argumentos]
```

## Common Options
- `-e archivo`: Verifica si el archivo existe.
- `-f archivo`: Comprueba si el archivo es un archivo regular.
- `-d directorio`: Verifica si el argumento es un directorio.
- `-z cadena`: Comprueba si la longitud de la cadena es cero.
- `-n cadena`: Verifica si la longitud de la cadena es mayor que cero.
- `a -o b`: Evalúa si al menos una de las expresiones es verdadera (AND).
- `a -a b`: Evalúa si ambas expresiones son verdaderas (OR).

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `test`:

1. **Verificar si un archivo existe:**
   ```bash
   test -e archivo.txt && echo "El archivo existe."
   ```

2. **Comprobar si un directorio existe:**
   ```bash
   test -d /ruta/al/directorio && echo "El directorio existe."
   ```

3. **Verificar si una cadena está vacía:**
   ```bash
   cadena=""
   test -z "$cadena" && echo "La cadena está vacía."
   ```

4. **Comparar números:**
   ```bash
   num1=5
   num2=10
   test $num1 -lt $num2 && echo "$num1 es menor que $num2."
   ```

5. **Comprobar si dos cadenas son iguales:**
   ```bash
   cadena1="hola"
   cadena2="hola"
   test "$cadena1" = "$cadena2" && echo "Las cadenas son iguales."
   ```

## Tips
- Utiliza `[` y `]` como una alternativa a `test`, por ejemplo: `[ -e archivo.txt ]`.
- Recuerda que el comando `test` devuelve un código de salida: 0 si la condición es verdadera y 1 si es falsa.
- Combina múltiples condiciones usando `-a` y `-o` para crear expresiones más complejas.
- Siempre encierra las variables entre comillas para evitar errores con espacios en blanco.