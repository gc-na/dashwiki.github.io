# [Español] Debian Almquist Shell (dash) curl uso: Obtener datos de URLs

## Overview
El comando `curl` se utiliza para transferir datos desde o hacia un servidor utilizando diversos protocolos, como HTTP, HTTPS, FTP, entre otros. Es una herramienta muy versátil que permite realizar solicitudes y obtener respuestas de manera sencilla.

## Usage
La sintaxis básica del comando `curl` es la siguiente:

```bash
curl [opciones] [argumentos]
```

## Common Options
A continuación se presentan algunas opciones comunes de `curl` junto con breves explicaciones:

- `-O`: Guarda el archivo descargado con el mismo nombre que tiene en el servidor.
- `-L`: Sigue redirecciones si el recurso solicitado ha cambiado de ubicación.
- `-I`: Muestra solo los encabezados de la respuesta HTTP.
- `-d`: Envía datos en una solicitud POST.
- `-H`: Añade un encabezado personalizado a la solicitud.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `curl`:

1. **Descargar un archivo:**

```bash
curl -O http://example.com/archivo.txt
```

2. **Seguir redirecciones:**

```bash
curl -L http://example.com
```

3. **Obtener solo los encabezados de una respuesta:**

```bash
curl -I http://example.com
```

4. **Enviar datos en una solicitud POST:**

```bash
curl -d "nombre=valor" http://example.com/api
```

5. **Añadir un encabezado personalizado:**

```bash
curl -H "Authorization: Bearer token" http://example.com/protegido
```

## Tips
- Utiliza la opción `-v` para ver información detallada sobre la conexión y la solicitud, lo que puede ser útil para depurar problemas.
- Si necesitas realizar múltiples solicitudes, considera usar un script para automatizar el proceso.
- Recuerda que `curl` puede manejar autenticación básica y otros métodos de autenticación, lo que lo hace muy útil para interactuar con APIs.