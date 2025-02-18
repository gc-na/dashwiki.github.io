# [Español] Debian Almquist Shell (dash) wget Uso: Descarga archivos desde la web

## Overview
El comando `wget` es una herramienta de línea de comandos utilizada para descargar archivos desde la web. Es especialmente útil para descargar contenido de manera no interactiva, lo que significa que puede ejecutarse en segundo plano o incluso en sesiones de terminal desconectadas.

## Usage
La sintaxis básica del comando `wget` es la siguiente:

```bash
wget [opciones] [argumentos]
```

## Common Options
A continuación se presentan algunas opciones comunes de `wget`:

- `-O <archivo>`: Especifica el nombre del archivo de salida.
- `-q`: Modo silencioso; no muestra mensajes de progreso.
- `-c`: Continúa una descarga interrumpida.
- `-r`: Descarga recursivamente todos los archivos de un directorio.
- `--limit-rate=<velocidad>`: Limita la velocidad de descarga a la cantidad especificada.

## Common Examples
Aquí hay algunos ejemplos prácticos de cómo usar `wget`:

1. **Descargar un archivo simple:**
   ```bash
   wget https://example.com/archivo.zip
   ```

2. **Descargar un archivo y guardarlo con un nombre específico:**
   ```bash
   wget -O mi_archivo.zip https://example.com/archivo.zip
   ```

3. **Descargar un archivo en modo silencioso:**
   ```bash
   wget -q https://example.com/archivo.zip
   ```

4. **Reanudar una descarga interrumpida:**
   ```bash
   wget -c https://example.com/archivo.zip
   ```

5. **Descargar todos los archivos de un sitio web de manera recursiva:**
   ```bash
   wget -r https://example.com/directorio/
   ```

## Tips
- Utiliza la opción `-q` para evitar mensajes innecesarios si estás descargando muchos archivos.
- Si descargas archivos grandes, considera usar `--limit-rate` para no saturar tu conexión a Internet.
- Para evitar problemas con el servidor, respeta las políticas de uso y limita la velocidad de descarga si es necesario.