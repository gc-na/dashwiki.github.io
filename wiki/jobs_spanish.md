# [Español] Debian Almquist Shell (dash) jobs uso: gestionar trabajos en segundo plano

## Overview
El comando `jobs` en el shell Debian Almquist (dash) se utiliza para mostrar la lista de trabajos que se están ejecutando en segundo plano en la sesión actual del terminal. Esto es útil para gestionar procesos que se han enviado al fondo y para ver su estado.

## Usage
La sintaxis básica del comando es la siguiente:
```
jobs [opciones] [argumentos]
```

## Common Options
- `-l`: Muestra el número de proceso (PID) de cada trabajo.
- `-n`: Muestra solo los trabajos que han cambiado de estado desde la última vez que se ejecutó el comando.
- `-p`: Muestra solo los PIDs de los trabajos.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `jobs`:

1. **Listar trabajos en segundo plano**:
   ```sh
   jobs
   ```

2. **Listar trabajos con números de proceso**:
   ```sh
   jobs -l
   ```

3. **Mostrar solo trabajos que han cambiado de estado**:
   ```sh
   jobs -n
   ```

4. **Obtener solo los PIDs de los trabajos**:
   ```sh
   jobs -p
   ```

## Tips
- Utiliza `bg %n` para reanudar un trabajo en segundo plano, donde `n` es el número del trabajo que quieres reanudar.
- Usa `fg %n` para traer un trabajo en segundo plano de vuelta al primer plano.
- Recuerda que los trabajos en segundo plano pueden ser interrumpidos con `Ctrl + Z`, lo que los suspenderá y los enviará a la lista de trabajos.