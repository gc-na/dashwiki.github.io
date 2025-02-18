# [Español] Debian Almquist Shell (dash) uptime Uso: Muestra el tiempo de actividad del sistema

## Overview
El comando `uptime` se utiliza para mostrar el tiempo que el sistema ha estado en funcionamiento desde el último arranque. También proporciona información sobre el número de usuarios conectados y la carga promedio del sistema en los últimos 1, 5 y 15 minutos.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
uptime [opciones]
```

## Common Options
- `-p`: Muestra el tiempo de actividad en un formato legible.
- `-s`: Muestra la fecha y hora del último arranque del sistema.

## Common Examples
A continuación se presentan algunos ejemplos prácticos del uso del comando `uptime`:

1. **Ver el tiempo de actividad del sistema:**
   ```bash
   uptime
   ```

2. **Mostrar el tiempo de actividad en un formato legible:**
   ```bash
   uptime -p
   ```

3. **Ver la fecha y hora del último arranque:**
   ```bash
   uptime -s
   ```

## Tips
- Utiliza `uptime` regularmente para monitorear el estado de tu sistema y asegurarte de que esté funcionando correctamente.
- Combina `uptime` con otros comandos como `top` o `htop` para obtener una visión más completa del rendimiento del sistema.
- Recuerda que el tiempo de actividad puede ser un indicador de estabilidad, pero no garantiza que el sistema esté libre de problemas.