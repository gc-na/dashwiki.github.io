# [Debian] Debian Almquist Shell (dash) en at: Programar tareas para ejecución futura

## Overview
El comando `at` se utiliza para programar la ejecución de comandos o scripts en un momento específico en el futuro. Es útil para tareas que no necesitan ejecutarse inmediatamente, permitiendo a los usuarios automatizar procesos de manera sencilla.

## Usage
La sintaxis básica del comando `at` es la siguiente:

```
at [opciones] [tiempo]
```

## Common Options
- `-f`: Especifica un archivo que contiene los comandos a ejecutar.
- `-m`: Envía un correo electrónico al usuario cuando se completa la tarea, incluso si no hay salida.
- `-q`: Permite especificar una cola de trabajo diferente para la tarea programada.
- `-l`: Muestra las tareas programadas para el usuario actual.
- `-d`: Elimina una tarea programada.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `at`:

1. **Programar un comando para que se ejecute a las 3 PM:**
   ```bash
   echo "echo 'Hola, mundo'" | at 15:00
   ```

2. **Programar un script para que se ejecute mañana a las 10 AM:**
   ```bash
   at 10:00 tomorrow -f /ruta/al/script.sh
   ```

3. **Listar las tareas programadas:**
   ```bash
   at -l
   ```

4. **Eliminar una tarea programada:**
   ```bash
   at -d 5
   ```
   (donde `5` es el ID de la tarea que se desea eliminar, obtenido de `at -l`).

## Tips
- Asegúrate de que el servicio `atd` esté en funcionamiento para que las tareas programadas se ejecuten correctamente.
- Utiliza el comando `atq` para ver las tareas pendientes y `atrm` para eliminarlas si es necesario.
- Puedes especificar el tiempo en formatos como "now + 1 hour" o "tomorrow" para mayor flexibilidad.