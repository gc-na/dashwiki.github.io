# [Debian] Debian Almquist Shell (dash) mount uso: Montar sistemas de archivos

## Overview
El comando `mount` se utiliza en sistemas Unix y Linux para montar sistemas de archivos en un punto de montaje específico en el sistema. Esto permite que el sistema operativo acceda a los datos almacenados en dispositivos de almacenamiento como discos duros, unidades USB y particiones.

## Usage
La sintaxis básica del comando `mount` es la siguiente:

```
mount [opciones] [dispositivo] [punto_de_montaje]
```

## Common Options
- `-t tipo`: Especifica el tipo de sistema de archivos a montar (por ejemplo, `ext4`, `ntfs`).
- `-o opciones`: Permite pasar opciones adicionales, como `ro` (solo lectura) o `rw` (lectura y escritura).
- `-a`: Monta todos los sistemas de archivos mencionados en `/etc/fstab`.
- `-r`: Monta el sistema de archivos en modo solo lectura.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `mount`:

1. Montar un dispositivo USB en `/mnt/usb`:
   ```bash
   mount /dev/sdb1 /mnt/usb
   ```

2. Montar una partición NTFS en modo lectura y escritura:
   ```bash
   mount -t ntfs -o rw /dev/sdc1 /mnt/ntfs
   ```

3. Montar todos los sistemas de archivos definidos en `/etc/fstab`:
   ```bash
   mount -a
   ```

4. Montar un sistema de archivos en modo solo lectura:
   ```bash
   mount -o ro /dev/sda1 /mnt/readonly
   ```

## Tips
- Asegúrate de que el punto de montaje exista antes de intentar montar un dispositivo.
- Utiliza el comando `umount` para desmontar un sistema de archivos de manera segura.
- Verifica los sistemas de archivos montados con el comando `df -h` para asegurarte de que se montaron correctamente.