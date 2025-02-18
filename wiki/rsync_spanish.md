# [Español] Debian Almquist Shell (dash) rsync Uso: Sincronización de archivos

## Overview
El comando `rsync` se utiliza para sincronizar archivos y directorios entre diferentes ubicaciones, ya sea en la misma máquina o entre máquinas remotas. Es especialmente útil para realizar copias de seguridad y transferencias eficientes, ya que solo copia los cambios realizados en los archivos.

## Usage
La sintaxis básica del comando `rsync` es la siguiente:

```bash
rsync [opciones] [origen] [destino]
```

## Common Options
A continuación se presentan algunas de las opciones más comunes de `rsync`:

- `-a`: Modo archivo; sincroniza recursivamente y preserva atributos como permisos y tiempos de modificación.
- `-v`: Modo verbose; muestra información detallada sobre el proceso de sincronización.
- `-z`: Comprime los datos durante la transferencia, lo que puede acelerar el proceso en conexiones lentas.
- `-r`: Sincroniza directorios de manera recursiva.
- `--delete`: Elimina archivos en el destino que no están presentes en el origen.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `rsync`:

1. Sincronizar un directorio local a otro directorio local:

   ```bash
   rsync -av /ruta/origen/ /ruta/destino/
   ```

2. Sincronizar un directorio local a un servidor remoto:

   ```bash
   rsync -av /ruta/origen/ usuario@servidor:/ruta/destino/
   ```

3. Sincronizar un directorio remoto a un directorio local:

   ```bash
   rsync -av usuario@servidor:/ruta/origen/ /ruta/destino/
   ```

4. Sincronizar y eliminar archivos en el destino que no están en el origen:

   ```bash
   rsync -av --delete /ruta/origen/ /ruta/destino/
   ```

## Tips
- Siempre es recomendable realizar una prueba con la opción `-n` (dry run) para ver qué archivos se copiarán sin realizar cambios reales.
- Utiliza la opción `-z` para mejorar la velocidad de transferencia en conexiones lentas.
- Considera usar `--progress` para ver el progreso de la transferencia, especialmente útil para archivos grandes.