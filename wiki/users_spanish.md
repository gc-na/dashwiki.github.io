# [Español] Usuarios de Debian Almquist Shell (dash): Muestra información sobre los usuarios conectados

## Overview
El comando `users` en el shell Debian Almquist (dash) se utiliza para mostrar los nombres de los usuarios que están actualmente conectados al sistema. Es una herramienta sencilla pero útil para obtener una visión rápida de quién está utilizando el sistema en un momento dado.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
users [opciones] [argumentos]
```

## Common Options
El comando `users` no tiene muchas opciones, pero aquí hay algunas que pueden ser útiles:

- `-a`: Muestra todos los nombres de usuario, incluso si están conectados a través de diferentes terminales.
- `-n`: No muestra el nombre de la terminal, solo los nombres de los usuarios.

## Common Examples

1. **Mostrar usuarios conectados:**
   Para ver los usuarios que están actualmente conectados al sistema, simplemente ejecuta:
   ```bash
   users
   ```

2. **Mostrar usuarios conectados con opción -a:**
   Para mostrar todos los usuarios conectados, incluyendo aquellos que pueden estar en diferentes terminales:
   ```bash
   users -a
   ```

3. **Mostrar usuarios sin nombre de terminal:**
   Si solo deseas ver los nombres de los usuarios sin detalles adicionales, puedes usar:
   ```bash
   users -n
   ```

## Tips
- Utiliza `users` en combinación con otros comandos como `who` o `w` para obtener información más detallada sobre los usuarios conectados.
- Este comando es especialmente útil en servidores donde múltiples usuarios pueden estar conectados simultáneamente.
- Recuerda que `users` solo muestra los usuarios que están conectados en el momento en que se ejecuta el comando; no proporciona un historial de conexiones.