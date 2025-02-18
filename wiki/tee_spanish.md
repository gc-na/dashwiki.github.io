# [Español] Debian Almquist Shell (dash) tee Uso equivalente: [redirigir y mostrar salida]

## Overview
El comando `tee` en el shell de Almquist de Debian (dash) se utiliza para leer la entrada estándar y escribirla tanto en la salida estándar como en uno o más archivos. Esto permite ver la salida de un comando mientras se guarda en un archivo.

## Usage
La sintaxis básica del comando `tee` es la siguiente:

```bash
tee [opciones] [argumentos]
```

## Common Options
- `-a`, `--append`: Añade la salida al final del archivo en lugar de sobrescribirlo.
- `-i`, `--ignore-interrupts`: Ignora las señales de interrupción.
- `-p`, `--output-error`: Controla el comportamiento en caso de error al escribir en el archivo.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `tee`:

1. **Guardar la salida de un comando en un archivo:**
   ```bash
   echo "Hola, mundo" | tee archivo.txt
   ```

2. **Guardar la salida y añadirla a un archivo existente:**
   ```bash
   echo "Nueva línea" | tee -a archivo.txt
   ```

3. **Ver la salida de un comando y guardarla al mismo tiempo:**
   ```bash
   ls -l | tee listado.txt
   ```

4. **Usar tee con múltiples archivos:**
   ```bash
   echo "Texto para varios archivos" | tee archivo1.txt archivo2.txt
   ```

## Tips
- Utiliza la opción `-a` si deseas agregar contenido a un archivo existente sin perder los datos previos.
- Puedes combinar `tee` con otros comandos usando tuberías para procesar la salida antes de guardarla.
- Recuerda que `tee` puede ser útil en scripts para registrar la salida de comandos mientras se sigue mostrando en la terminal.