# [Español] Debian Almquist Shell (dash) netcat uso: Herramienta de red versátil

## Overview
El comando netcat, también conocido como "nc", es una herramienta de red que permite leer y escribir datos a través de conexiones de red utilizando el protocolo TCP o UDP. Es útil para depuración, transferencia de archivos y creación de conexiones de red.

## Usage
La sintaxis básica del comando netcat es la siguiente:

```bash
netcat [opciones] [argumentos]
```

## Common Options
- `-l`: Escuchar en un puerto específico.
- `-p`: Especificar el puerto local.
- `-u`: Usar el protocolo UDP en lugar de TCP.
- `-v`: Modo verbose, proporciona más información sobre la conexión.
- `-z`: Modo de escaneo, no envía datos, solo verifica si el puerto está abierto.

## Common Examples
1. **Escuchar en un puerto específico**:
   ```bash
   netcat -l -p 1234
   ```
   Este comando pone a netcat en modo escucha en el puerto 1234.

2. **Conectar a un servidor**:
   ```bash
   netcat example.com 80
   ```
   Este comando establece una conexión TCP al puerto 80 del servidor `example.com`.

3. **Enviar un archivo**:
   ```bash
   netcat -l -p 1234 > archivo_recibido.txt
   ```
   En otro terminal, puedes enviar un archivo con:
   ```bash
   netcat localhost 1234 < archivo_a_enviar.txt
   ```

4. **Escaneo de puertos**:
   ```bash
   netcat -z -v example.com 1-1000
   ```
   Este comando escanea los puertos del 1 al 1000 en `example.com` para verificar cuáles están abiertos.

## Tips
- Asegúrate de tener los permisos necesarios para escuchar en puertos por debajo de 1024.
- Usa el modo verbose (`-v`) para obtener información adicional que puede ser útil para depuración.
- Recuerda que netcat puede ser utilizado tanto para conexiones TCP como UDP, así que elige el protocolo adecuado según tus necesidades.