# [Español] Debian Almquist Shell (dash) hostname uso: Obtener o establecer el nombre del host

## Overview
El comando `hostname` se utiliza para mostrar o establecer el nombre del host del sistema. El nombre del host es una etiqueta que identifica un dispositivo en una red.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
hostname [opciones] [argumentos]
```

## Common Options
- `-f`, `--fqdn`: Muestra el nombre de dominio completamente calificado (FQDN).
- `-i`, `--ip-address`: Muestra la dirección IP del host.
- `-s`, `--short`: Muestra solo el nombre corto del host.
- `-y`, `--yp`: Muestra el nombre del host de NIS.

## Common Examples
1. **Mostrar el nombre del host actual:**
   ```bash
   hostname
   ```

2. **Mostrar el nombre de dominio completamente calificado:**
   ```bash
   hostname -f
   ```

3. **Mostrar la dirección IP del host:**
   ```bash
   hostname -i
   ```

4. **Establecer un nuevo nombre de host:**
   ```bash
   hostname nuevo-nombre
   ```

5. **Mostrar solo el nombre corto del host:**
   ```bash
   hostname -s
   ```

## Tips
- Para que los cambios en el nombre del host sean permanentes, es recomendable editar el archivo `/etc/hostname`.
- Después de cambiar el nombre del host, es posible que necesites reiniciar el sistema o reiniciar el servicio de red para que los cambios surtan efecto.
- Utiliza `hostnamectl` en sistemas más recientes para gestionar el nombre del host de manera más avanzada.