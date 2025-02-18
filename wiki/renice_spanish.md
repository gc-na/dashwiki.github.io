# [Debian] Debian Almquist Shell (dash) renice: Cambiar la prioridad de un proceso

## Overview
El comando `renice` se utiliza para cambiar la prioridad de ejecución de uno o más procesos en un sistema Unix-like. La prioridad determina la cantidad de tiempo de CPU que un proceso puede utilizar en comparación con otros procesos. Un número de prioridad más bajo significa mayor prioridad.

## Usage
La sintaxis básica del comando `renice` es la siguiente:

```bash
renice [opciones] [valores] [PID...]
```

- `[valores]`: el nuevo valor de prioridad que se desea asignar.
- `[PID...]`: uno o más identificadores de proceso a los que se les cambiará la prioridad.

## Common Options
- `-n`, `--priority`: Especifica el nuevo valor de prioridad. Puede ser un número entre -20 (máxima prioridad) y 19 (mínima prioridad).
- `-p`, `--pid`: Permite especificar uno o más PIDs de los procesos a los que se les cambiará la prioridad.
- `-g`, `--pgrp`: Cambia la prioridad de todos los procesos en el grupo de procesos especificado.
- `-u`, `--user`: Cambia la prioridad de todos los procesos del usuario especificado.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `renice`:

1. **Cambiar la prioridad de un proceso específico:**
   ```bash
   renice -n 10 -p 1234
   ```
   Este comando cambia la prioridad del proceso con PID 1234 a 10.

2. **Cambiar la prioridad de varios procesos:**
   ```bash
   renice -n 5 -p 1234 5678 91011
   ```
   Cambia la prioridad de los procesos con PIDs 1234, 5678 y 91011 a 5.

3. **Cambiar la prioridad de todos los procesos de un usuario:**
   ```bash
   renice -n 15 -u nombre_usuario
   ```
   Este comando establece la prioridad de todos los procesos del usuario `nombre_usuario` a 15.

4. **Cambiar la prioridad de un grupo de procesos:**
   ```bash
   renice -n -5 -g 1234
   ```
   Cambia la prioridad de todos los procesos en el grupo de procesos con ID 1234 a -5.

## Tips
- Asegúrate de tener los permisos necesarios para cambiar la prioridad de los procesos. Generalmente, solo el usuario propietario del proceso o el usuario root pueden hacerlo.
- Utiliza valores de prioridad con cuidado; asignar una prioridad demasiado alta a un proceso puede afectar negativamente el rendimiento del sistema.
- Puedes verificar la prioridad actual de un proceso usando el comando `ps` con la opción `-o` para mostrar la columna de prioridad.