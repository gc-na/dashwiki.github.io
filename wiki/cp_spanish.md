# [Español] Debian Almquist Shell (dash) cp Uso: Copiar archivos y directorios

## Overview
El comando `cp` se utiliza para copiar archivos y directorios en el sistema de archivos. Permite crear duplicados de archivos existentes o mover contenido entre diferentes ubicaciones.

## Usage
La sintaxis básica del comando `cp` es la siguiente:

```bash
cp [opciones] [orígenes] [destino]
```

## Common Options
- `-r`: Copia directorios de manera recursiva.
- `-i`: Solicita confirmación antes de sobrescribir archivos existentes.
- `-u`: Copia solo si el archivo de origen es más reciente que el archivo de destino o si el archivo de destino no existe.
- `-v`: Muestra los archivos que se están copiando (modo verbose).

## Common Examples
- Copiar un archivo a otro archivo:
  ```bash
  cp archivo1.txt archivo2.txt
  ```

- Copiar un archivo a un directorio:
  ```bash
  cp archivo1.txt /ruta/al/directorio/
  ```

- Copiar un directorio y su contenido de manera recursiva:
  ```bash
  cp -r directorio1/ directorio2/
  ```

- Copiar un archivo y pedir confirmación antes de sobrescribir:
  ```bash
  cp -i archivo1.txt archivo2.txt
  ```

- Copiar solo archivos más recientes:
  ```bash
  cp -u archivo1.txt archivo2.txt
  ```

## Tips
- Siempre verifica la ruta del destino para evitar sobrescribir archivos importantes.
- Usa la opción `-v` para tener un registro visual de los archivos que se están copiando, especialmente útil en operaciones grandes.
- Considera usar `-r` con cuidado, ya que puede copiar grandes cantidades de datos si no se especifica correctamente.