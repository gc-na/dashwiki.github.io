# [Debian] Debian Almquist Shell (dash) sftp uso: Transferir archivos de forma segura

## Overview
El comando `sftp` (Secure File Transfer Protocol) se utiliza para transferir archivos de manera segura entre un cliente y un servidor a través de una conexión SSH. Proporciona una interfaz similar a la de FTP, pero con la ventaja de la encriptación, lo que garantiza que los datos sean transmitidos de manera segura.

## Usage
La sintaxis básica del comando `sftp` es la siguiente:

```
sftp [opciones] [usuario@servidor]
```

## Common Options
- `-P [puerto]`: Especifica el puerto a utilizar para la conexión.
- `-i [archivo]`: Utiliza un archivo de clave privada específico para la autenticación.
- `-o [opción]`: Permite pasar opciones adicionales a la conexión SSH.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `sftp`:

1. **Conectar a un servidor SFTP:**
   ```bash
   sftp usuario@servidor.com
   ```

2. **Transferir un archivo desde el cliente al servidor:**
   ```bash
   sftp usuario@servidor.com
   put archivo.txt
   ```

3. **Descargar un archivo del servidor al cliente:**
   ```bash
   sftp usuario@servidor.com
   get archivo.txt
   ```

4. **Listar archivos en el directorio remoto:**
   ```bash
   sftp usuario@servidor.com
   ls
   ```

5. **Cambiar al directorio remoto:**
   ```bash
   sftp usuario@servidor.com
   cd /ruta/del/directorio
   ```

## Tips
- Asegúrate de tener configuradas las claves SSH para evitar ingresar la contraseña cada vez que te conectes.
- Utiliza el comando `lcd` para cambiar el directorio local antes de transferir archivos.
- Familiarízate con los comandos internos de `sftp` como `mget` y `mput` para transferir múltiples archivos a la vez.