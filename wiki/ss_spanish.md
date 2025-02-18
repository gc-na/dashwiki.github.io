# [Español] Debian Almquist Shell (dash) ss Uso equivalente: [visualizar conexiones de red]

## Overview
El comando `ss` se utiliza para investigar sockets en Linux. Permite mostrar información sobre las conexiones de red, tanto TCP como UDP, así como los sockets de escucha y otras estadísticas de red.

## Usage
La sintaxis básica del comando es:

```bash
ss [opciones] [argumentos]
```

## Common Options
- `-t`: Muestra conexiones TCP.
- `-u`: Muestra conexiones UDP.
- `-l`: Muestra solo sockets en escucha.
- `-p`: Muestra el proceso que está utilizando el socket.
- `-n`: Muestra direcciones y puertos en formato numérico, evitando la resolución de nombres.

## Common Examples

1. **Mostrar todas las conexiones TCP:**
   ```bash
   ss -t
   ```

2. **Mostrar todas las conexiones UDP:**
   ```bash
   ss -u
   ```

3. **Mostrar sockets en escucha:**
   ```bash
   ss -l
   ```

4. **Mostrar conexiones TCP con información del proceso:**
   ```bash
   ss -tp
   ```

5. **Mostrar todas las conexiones en formato numérico:**
   ```bash
   ss -n
   ```

## Tips
- Utiliza la opción `-p` para identificar qué procesos están utilizando las conexiones, lo que puede ser útil para la resolución de problemas.
- Combina opciones para obtener información más detallada, por ejemplo, `ss -tunlp` para ver todas las conexiones TCP y UDP junto con los procesos.
- Revisa regularmente las conexiones de red en tu sistema para detectar actividad inusual o no autorizada.