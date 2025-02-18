# [Debian] Debian Almquist Shell (dash) nice uso: Ajustar la prioridad de ejecución de procesos

## Overview
El comando `nice` se utiliza en sistemas Unix y Linux para ejecutar un programa con una prioridad de CPU ajustada. Esto permite que los usuarios controlen la cantidad de recursos del sistema que un proceso puede consumir, lo que es especialmente útil en entornos multitarea.

## Usage
La sintaxis básica del comando `nice` es la siguiente:

```bash
nice [opciones] [comando] [argumentos]
```

## Common Options
- `-n, --adjustment=N`: Establece el nivel de ajuste de la prioridad. El valor puede ser un número positivo o negativo. Un número más bajo significa mayor prioridad.
- `-h, --help`: Muestra la ayuda sobre el uso del comando.
- `--version`: Muestra la versión del comando.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `nice`:

1. **Ejecutar un comando con prioridad baja:**
   ```bash
   nice -n 19 myscript.sh
   ```
   Este comando ejecuta `myscript.sh` con la prioridad más baja posible.

2. **Ejecutar un comando con prioridad normal:**
   ```bash
   nice myprogram
   ```
   Esto ejecuta `myprogram` con la prioridad predeterminada (0).

3. **Ajustar la prioridad de un proceso en ejecución:**
   ```bash
   renice 10 -p 1234
   ```
   Cambia la prioridad del proceso con ID 1234 a 10.

4. **Ejecutar un comando con prioridad alta:**
   ```bash
   nice -n -5 myhighprioritytask
   ```
   Este comando ejecuta `myhighprioritytask` con una prioridad más alta.

## Tips
- Utiliza `nice` para evitar que procesos intensivos en recursos afecten el rendimiento del sistema.
- Recuerda que solo el usuario root puede establecer prioridades negativas.
- Verifica la prioridad de los procesos en ejecución utilizando el comando `top` o `ps`.