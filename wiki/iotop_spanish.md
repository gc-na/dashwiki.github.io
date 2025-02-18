# [Debian] Debian Almquist Shell (dash) iotop Uso: Monitorear el uso de I/O de procesos

## Overview
El comando `iotop` se utiliza para monitorear el uso de entrada/salida (I/O) de los procesos en un sistema Linux. Permite visualizar qué procesos están consumiendo más recursos de disco, lo que puede ser útil para identificar cuellos de botella en el rendimiento del sistema.

## Usage
La sintaxis básica del comando `iotop` es la siguiente:

```bash
iotop [opciones] [argumentos]
```

## Common Options
- `-o`: Muestra solo los procesos que están realizando operaciones de I/O.
- `-b`: Ejecuta `iotop` en modo batch, ideal para redirección a un archivo.
- `-n NUM`: Especifica el número de iteraciones en modo batch.
- `-d SEG`: Define el intervalo de actualización en segundos.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `iotop`:

1. **Ejecutar iotop en modo interactivo**:
   ```bash
   iotop
   ```

2. **Mostrar solo procesos que están realizando I/O**:
   ```bash
   iotop -o
   ```

3. **Ejecutar iotop en modo batch y guardar la salida en un archivo**:
   ```bash
   iotop -b -n 10 > iotop_output.txt
   ```

4. **Actualizar cada 2 segundos en modo interactivo**:
   ```bash
   iotop -d 2
   ```

## Tips
- Asegúrate de ejecutar `iotop` con privilegios de superusuario (usando `sudo`) para obtener información completa sobre todos los procesos.
- Utiliza el modo batch si necesitas registrar el uso de I/O durante un período prolongado.
- Combina `iotop` con otras herramientas como `grep` para filtrar la salida y encontrar procesos específicos.