# [Español] Debian Almquist Shell (dash) killall Uso: Terminar procesos por nombre

## Overview
El comando `killall` se utiliza para terminar procesos en ejecución basados en su nombre. A diferencia de otros comandos que requieren un identificador de proceso (PID), `killall` permite especificar el nombre del proceso que se desea finalizar, lo que facilita la gestión de múltiples instancias de un mismo programa.

## Usage
La sintaxis básica del comando `killall` es la siguiente:

```bash
killall [opciones] [nombre_del_proceso]
```

## Common Options
A continuación se presentan algunas opciones comunes que se pueden utilizar con `killall`:

- `-9`: Fuerza la terminación del proceso (SIGKILL).
- `-v`: Muestra información detallada sobre los procesos que se están terminando.
- `-i`: Pide confirmación antes de terminar cada proceso.
- `-r`: Permite usar expresiones regulares para especificar el nombre del proceso.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `killall`:

1. Terminar todos los procesos de Firefox:
   ```bash
   killall firefox
   ```

2. Forzar la terminación de todos los procesos de un programa específico:
   ```bash
   killall -9 nombre_del_proceso
   ```

3. Mostrar información detallada al terminar procesos:
   ```bash
   killall -v nombre_del_proceso
   ```

4. Usar una expresión regular para terminar procesos que comienzan con "test":
   ```bash
   killall -r '^test.*'
   ```

5. Pedir confirmación antes de terminar cada proceso:
   ```bash
   killall -i nombre_del_proceso
   ```

## Tips
- Siempre verifica qué procesos se están ejecutando antes de usar `killall` para evitar terminar procesos importantes accidentalmente.
- Utiliza la opción `-v` para tener un mejor control y visibilidad sobre qué procesos se están terminando.
- Si no estás seguro del nombre exacto del proceso, puedes usar el comando `ps` para listar los procesos en ejecución antes de usar `killall`.