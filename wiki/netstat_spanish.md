# [Debian] Debian Almquist Shell (dash) netstat Uso: Muestra conexiones de red

## Overview
El comando `netstat` se utiliza para mostrar información sobre las conexiones de red, las tablas de enrutamiento y las estadísticas de interfaz. Es una herramienta útil para diagnosticar problemas de red y monitorizar el estado de las conexiones.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
netstat [opciones] [argumentos]
```

## Common Options
- `-a`: Muestra todas las conexiones y puertos de escucha.
- `-t`: Muestra solo las conexiones TCP.
- `-u`: Muestra solo las conexiones UDP.
- `-n`: Muestra las direcciones y números de puerto en formato numérico.
- `-l`: Muestra solo los puertos que están en estado de escucha.
- `-p`: Muestra el identificador del proceso (PID) y el nombre del programa que está utilizando la conexión.

## Common Examples
- Para mostrar todas las conexiones y puertos de escucha:
  ```bash
  netstat -a
  ```

- Para mostrar solo las conexiones TCP:
  ```bash
  netstat -t
  ```

- Para mostrar conexiones UDP en formato numérico:
  ```bash
  netstat -un
  ```

- Para ver solo los puertos en estado de escucha:
  ```bash
  netstat -l
  ```

- Para mostrar las conexiones junto con el PID y el nombre del programa:
  ```bash
  netstat -p
  ```

## Tips
- Utiliza `netstat -tuln` para obtener una vista combinada de las conexiones TCP y UDP en estado de escucha, mostrando los números de puerto en formato numérico.
- Puedes combinar opciones para obtener información más específica, por ejemplo, `netstat -at` para ver solo las conexiones TCP activas.
- Recuerda que algunos sistemas pueden requerir permisos de superusuario para mostrar información completa sobre las conexiones y procesos.