# [Debian] Debian Almquist Shell (dash) dig <Uso equivalente en español>: consulta de DNS

## Overview
El comando `dig` (Domain Information Groper) es una herramienta utilizada para realizar consultas DNS (Sistema de Nombres de Dominio). Permite a los usuarios obtener información sobre registros DNS, como direcciones IP, registros MX y más.

## Usage
La sintaxis básica del comando `dig` es la siguiente:

```bash
dig [opciones] [argumentos]
```

## Common Options
- `@servidor`: Especifica el servidor DNS al que se enviará la consulta.
- `-t tipo`: Define el tipo de registro DNS que se desea consultar (por ejemplo, A, AAAA, MX).
- `+short`: Muestra una salida más concisa, mostrando solo la información esencial.
- `+trace`: Realiza un seguimiento de la consulta a través de los servidores DNS.

## Common Examples
Aquí tienes algunos ejemplos prácticos del uso del comando `dig`:

1. **Consulta de una dirección IP (registro A)**:
   ```bash
   dig example.com
   ```

2. **Consulta de registros MX (Mail Exchange)**:
   ```bash
   dig -t MX example.com
   ```

3. **Consulta a un servidor DNS específico**:
   ```bash
   dig @8.8.8.8 example.com
   ```

4. **Consulta con salida corta**:
   ```bash
   dig +short example.com
   ```

5. **Seguimiento de la consulta DNS**:
   ```bash
   dig +trace example.com
   ```

## Tips
- Utiliza `+short` para obtener resultados más limpios y fáciles de leer.
- Si estás depurando problemas de DNS, el uso de `+trace` puede ayudarte a entender cómo se resuelve la consulta.
- Recuerda que puedes consultar diferentes tipos de registros DNS utilizando la opción `-t`, lo que te permite obtener información específica según tus necesidades.