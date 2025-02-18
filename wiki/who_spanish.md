# [Debian] Debian Almquist Shell (dash) who: Muestra quién está conectado

## Overview
El comando `who` en el shell Almquist de Debian (dash) se utiliza para mostrar información sobre los usuarios que están actualmente conectados al sistema. Proporciona detalles como el nombre de usuario, la terminal, la fecha y hora de inicio de sesión, y la dirección IP o nombre del host desde el que se conectaron.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
who [opciones] [argumentos]
```

## Common Options
- `-b`: Muestra la última vez que se reinició el sistema.
- `-H`: Muestra los encabezados de las columnas.
- `--help`: Muestra la ayuda sobre el uso del comando.
- `--version`: Muestra la versión del comando.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `who`:

1. Mostrar todos los usuarios conectados:
   ```bash
   who
   ```

2. Mostrar la última vez que se reinició el sistema:
   ```bash
   who -b
   ```

3. Mostrar los encabezados de las columnas:
   ```bash
   who -H
   ```

4. Mostrar información de un usuario específico:
   ```bash
   who username
   ```

## Tips
- Utiliza `who -H` para obtener una vista más clara con encabezados, especialmente si hay muchos usuarios conectados.
- Combina `who` con otros comandos como `grep` para filtrar resultados específicos.
- Revisa la salida de `who` para monitorear la actividad de los usuarios en sistemas compartidos.