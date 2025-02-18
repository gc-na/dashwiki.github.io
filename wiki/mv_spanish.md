# [Español] Debian Almquist Shell (dash) mv Uso: Mover o renombrar archivos y directorios

## Overview
El comando `mv` se utiliza en el shell para mover o renombrar archivos y directorios. Es una herramienta fundamental para la gestión de archivos en sistemas Unix y Linux.

## Usage
La sintaxis básica del comando `mv` es la siguiente:

```bash
mv [opciones] [origen] [destino]
```

## Common Options
- `-i`: Pregunta antes de sobrescribir un archivo existente.
- `-u`: Mueve solo si el archivo de origen es más nuevo que el archivo de destino o si el archivo de destino no existe.
- `-v`: Muestra el proceso de movimiento, indicando qué archivos se están moviendo.

## Common Examples
1. **Mover un archivo a un directorio:**
   ```bash
   mv archivo.txt /ruta/al/directorio/
   ```

2. **Renombrar un archivo:**
   ```bash
   mv archivo_viejo.txt archivo_nuevo.txt
   ```

3. **Mover varios archivos a un directorio:**
   ```bash
   mv archivo1.txt archivo2.txt /ruta/al/directorio/
   ```

4. **Mover un directorio y su contenido:**
   ```bash
   mv /ruta/al/directorio_origen/ /ruta/al/directorio_destino/
   ```

5. **Usar la opción interactiva para evitar sobrescribir:**
   ```bash
   mv -i archivo.txt /ruta/al/directorio/
   ```

## Tips
- Siempre verifica el destino antes de mover archivos para evitar pérdidas accidentales.
- Usa la opción `-v` para tener un registro de las acciones realizadas, especialmente cuando mueves múltiples archivos.
- Si estás renombrando archivos, asegúrate de que el nuevo nombre no exista en la misma ubicación para evitar sobrescrituras no deseadas.