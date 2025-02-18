# [Español] Debian Almquist Shell (dash) ftp uso: Transferir archivos a través de la red

## Overview
El comando `ftp` (File Transfer Protocol) se utiliza para transferir archivos entre un cliente y un servidor a través de una red. Permite a los usuarios conectarse a un servidor FTP, navegar por los directorios y transferir archivos de manera sencilla.

## Usage
La sintaxis básica del comando `ftp` es la siguiente:

```bash
ftp [opciones] [argumentos]
```

## Common Options
- `-i`: Desactiva el modo interactivo, lo que permite transferir múltiples archivos sin confirmación.
- `-v`: Muestra información detallada sobre la conexión y la transferencia de archivos.
- `-n`: Evita la conexión automática al servidor al inicio, útil para scripts.
- `-p`: Utiliza el modo pasivo para la transferencia de archivos, lo que puede ayudar a evitar problemas de firewall.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `ftp`:

1. Conectar a un servidor FTP:
   ```bash
   ftp ftp.ejemplo.com
   ```

2. Subir un archivo al servidor:
   ```bash
   put archivo.txt
   ```

3. Descargar un archivo del servidor:
   ```bash
   get archivo.txt
   ```

4. Cambiar al modo binario para transferir archivos:
   ```bash
   binary
   ```

5. Listar los archivos en el directorio actual del servidor:
   ```bash
   ls
   ```

## Tips
- Siempre utiliza el modo binario (`binary`) al transferir archivos que no son de texto, como imágenes o ejecutables, para evitar la corrupción de datos.
- Si tienes problemas de conexión, considera usar el modo pasivo (`passive`) para evitar restricciones de firewall.
- Recuerda cerrar la sesión correctamente con el comando `bye` o `quit` para evitar conexiones abiertas innecesarias.