# [Español] Debian Almquist Shell (dash) id uso: Muestra información del usuario

## Overview
El comando `id` se utiliza para mostrar información sobre el usuario actual o un usuario específico. Proporciona detalles como el UID (Identificador de Usuario), GID (Identificador de Grupo) y los grupos a los que pertenece el usuario.

## Usage
La sintaxis básica del comando es la siguiente:

```
id [opciones] [usuario]
```

## Common Options
- `-u`: Muestra solo el UID del usuario.
- `-g`: Muestra solo el GID del grupo principal del usuario.
- `-G`: Muestra todos los GIDs de los grupos a los que pertenece el usuario.
- `-n`: Muestra el nombre en lugar del número (puede usarse con `-u` o `-g`).

## Common Examples
1. Mostrar información del usuario actual:
   ```bash
   id
   ```

2. Mostrar solo el UID del usuario actual:
   ```bash
   id -u
   ```

3. Mostrar solo el GID del grupo principal del usuario actual:
   ```bash
   id -g
   ```

4. Mostrar todos los GIDs de los grupos a los que pertenece el usuario actual:
   ```bash
   id -G
   ```

5. Mostrar información de un usuario específico (por ejemplo, "usuario1"):
   ```bash
   id usuario1
   ```

## Tips
- Utiliza `id` sin opciones para obtener un resumen completo de la información del usuario.
- Combina opciones, como `id -Gn`, para obtener una lista de nombres de grupos en lugar de números.
- Si necesitas verificar los permisos de un usuario, el comando `id` es una herramienta rápida y efectiva.