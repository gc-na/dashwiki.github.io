# [Español] Debian Almquist Shell (dash) ps Uso: [mostrar procesos en ejecución]

## Overview
El comando `ps` se utiliza para mostrar información sobre los procesos en ejecución en el sistema. Permite a los usuarios ver qué procesos están activos, su estado y otros detalles relevantes.

## Usage
La sintaxis básica del comando `ps` es la siguiente:

```bash
ps [opciones] [argumentos]
```

## Common Options
A continuación se presentan algunas opciones comunes para el comando `ps`:

- `-e`: Muestra todos los procesos en el sistema.
- `-f`: Muestra información completa sobre los procesos.
- `-u [usuario]`: Muestra los procesos de un usuario específico.
- `-aux`: Muestra todos los procesos con detalles adicionales (incluyendo los de otros usuarios).
- `--sort`: Permite ordenar la salida según un criterio específico.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `ps`:

1. Mostrar todos los procesos en ejecución:
   ```bash
   ps -e
   ```

2. Mostrar procesos con información completa:
   ```bash
   ps -f
   ```

3. Mostrar procesos de un usuario específico:
   ```bash
   ps -u nombre_usuario
   ```

4. Mostrar todos los procesos con detalles adicionales:
   ```bash
   ps aux
   ```

5. Ordenar la salida por uso de memoria:
   ```bash
   ps aux --sort=-%mem
   ```

## Tips
- Utiliza `ps aux` para obtener una vista completa de todos los procesos, incluyendo los de otros usuarios.
- Combina `ps` con otros comandos como `grep` para filtrar resultados específicos, por ejemplo:
  ```bash
  ps aux | grep nombre_proceso
  ```
- Familiarízate con las opciones disponibles para personalizar la salida según tus necesidades.