# [Debian] Debian Almquist Shell (dash) traceroute6 uso: rastrear rutas de paquetes IPv6

## Overview
El comando `traceroute6` se utiliza para rastrear la ruta que toman los paquetes de datos a través de una red IPv6. Muestra cada salto que realiza un paquete desde el origen hasta el destino, lo que permite identificar posibles problemas de conectividad y latencia en la red.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
traceroute6 [opciones] [argumentos]
```

## Common Options
- `-n`: No resuelve nombres de host, mostrando solo direcciones IP.
- `-m <n>`: Establece el número máximo de saltos (hops) a seguir.
- `-p <puerto>`: Especifica el puerto a utilizar para el envío de paquetes.
- `-w <segundos>`: Define el tiempo de espera para cada respuesta.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `traceroute6`:

1. Rastrear la ruta a un host específico:
   ```bash
   traceroute6 www.ejemplo.com
   ```

2. Rastrear la ruta sin resolver nombres de host:
   ```bash
   traceroute6 -n www.ejemplo.com
   ```

3. Establecer un número máximo de saltos:
   ```bash
   traceroute6 -m 15 www.ejemplo.com
   ```

4. Especificar un puerto para el envío de paquetes:
   ```bash
   traceroute6 -p 80 www.ejemplo.com
   ```

5. Ajustar el tiempo de espera para respuestas:
   ```bash
   traceroute6 -w 2 www.ejemplo.com
   ```

## Tips
- Utiliza la opción `-n` para obtener resultados más rápidos, ya que evitarás la resolución de nombres de host.
- Si estás experimentando problemas de conectividad, prueba aumentar el número máximo de saltos con `-m`.
- Recuerda que algunos routers pueden bloquear paquetes de `traceroute`, lo que puede resultar en saltos perdidos o respuestas incompletas.