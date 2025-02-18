# [Español] Debian Almquist Shell (dash) mtr Uso: Herramienta de diagnóstico de red

## Overview
El comando `mtr` combina las funcionalidades de `ping` y `traceroute`, permitiendo a los usuarios diagnosticar problemas de red al mostrar la ruta que toman los paquetes hacia un destino y el tiempo que tardan en cada salto.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
mtr [opciones] [destino]
```

## Common Options
- `-r`: Ejecuta `mtr` en modo reporte, mostrando un resumen al final.
- `-c <n>`: Especifica el número de pings a enviar, donde `<n>` es un número entero.
- `-i <segundos>`: Define el intervalo entre pings en segundos.
- `-p`: Muestra el número de puerto en la salida.
- `-n`: No resuelve nombres de host, solo muestra direcciones IP.

## Common Examples
1. **Ejecutar mtr a un destino específico**:
   ```bash
   mtr example.com
   ```

2. **Ejecutar mtr en modo reporte, enviando 10 pings**:
   ```bash
   mtr -r -c 10 example.com
   ```

3. **Ejecutar mtr sin resolver nombres de host**:
   ```bash
   mtr -n example.com
   ```

4. **Ejecutar mtr con un intervalo de 2 segundos entre pings**:
   ```bash
   mtr -i 2 example.com
   ```

## Tips
- Utiliza el modo reporte (`-r`) para obtener un resumen claro de la calidad de la conexión.
- Si estás diagnosticando problemas de red, prueba con diferentes destinos para ver si el problema es específico de una ruta.
- Recuerda que el uso de `-n` puede acelerar el proceso al evitar la resolución de nombres de dominio, especialmente en redes lentas.