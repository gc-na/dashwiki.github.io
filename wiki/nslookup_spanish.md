# [Debian] Debian Almquist Shell (dash) nslookup Uso: Consulta de información de DNS

## Overview
El comando `nslookup` se utiliza para consultar información sobre el Sistema de Nombres de Dominio (DNS). Permite a los usuarios obtener detalles sobre direcciones IP, nombres de dominio y otros registros DNS.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
nslookup [opciones] [argumentos]
```

## Common Options
- `-type=tipo`: Especifica el tipo de registro DNS que deseas consultar (por ejemplo, A, MX, CNAME).
- `-timeout=segundos`: Establece el tiempo de espera para las respuestas del servidor DNS.
- `-retry=número`: Define cuántas veces se intentará consultar el servidor DNS en caso de fallo.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `nslookup`:

1. **Consultar la dirección IP de un dominio:**
   ```bash
   nslookup ejemplo.com
   ```

2. **Consultar registros de tipo MX (Mail Exchange) para un dominio:**
   ```bash
   nslookup -type=MX ejemplo.com
   ```

3. **Consultar un registro específico (CNAME) para un dominio:**
   ```bash
   nslookup -type=CNAME www.ejemplo.com
   ```

4. **Cambiar el servidor DNS para la consulta:**
   ```bash
   nslookup ejemplo.com 8.8.8.8
   ```

## Tips
- Utiliza `nslookup` en modo interactivo simplemente ejecutando `nslookup` sin argumentos para realizar múltiples consultas sin tener que volver a escribir el comando.
- Recuerda que algunos registros pueden no estar disponibles si no están configurados correctamente en el servidor DNS.
- Si necesitas información más detallada, considera usar la opción `-debug` para obtener más información sobre el proceso de consulta.