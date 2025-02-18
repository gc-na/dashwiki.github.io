# [Debian] Debian Almquist Shell (dash) top uso: Muestra procesos en tiempo real

## Overview
El comando `top` es una herramienta que permite monitorear los procesos en ejecución en un sistema Unix-like. Muestra información en tiempo real sobre el uso de la CPU, la memoria y otros recursos del sistema, lo que facilita la identificación de procesos que consumen muchos recursos.

## Usage
La sintaxis básica del comando `top` es la siguiente:

```bash
top [opciones]
```

## Common Options
A continuación se presentan algunas opciones comunes que se pueden utilizar con el comando `top`:

- `-d <segundos>`: Establece el intervalo de actualización en segundos.
- `-n <número>`: Especifica el número de actualizaciones que se deben realizar antes de salir.
- `-u <usuario>`: Muestra solo los procesos pertenecientes al usuario especificado.
- `-p <PID>`: Muestra solo el proceso con el ID de proceso especificado.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `top`:

1. **Ejecutar top con la configuración predeterminada:**
   ```bash
   top
   ```

2. **Actualizar la visualización cada 2 segundos:**
   ```bash
   top -d 2
   ```

3. **Mostrar solo los procesos de un usuario específico:**
   ```bash
   top -u nombre_usuario
   ```

4. **Limitar la visualización a un proceso específico:**
   ```bash
   top -p 1234
   ```

5. **Ejecutar top y salir después de 5 actualizaciones:**
   ```bash
   top -n 5
   ```

## Tips
- Utiliza la tecla `h` mientras estás en `top` para acceder a la ayuda y ver más opciones disponibles.
- Puedes ordenar los procesos por uso de CPU o memoria presionando las teclas `Shift + P` o `Shift + M`, respectivamente.
- Para salir de la interfaz de `top`, simplemente presiona `q`.