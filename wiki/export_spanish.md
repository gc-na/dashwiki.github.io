# [Español] Debian Almquist Shell (dash) export Uso equivalente: Establecer variables de entorno

## Overview
El comando `export` en el shell Debian Almquist (dash) se utiliza para establecer variables de entorno que estarán disponibles para los procesos hijos. Esto es útil para configurar el entorno de ejecución de programas y scripts.

## Usage
La sintaxis básica del comando `export` es la siguiente:

```bash
export [opciones] [argumentos]
```

## Common Options
- `-n`: Elimina la exportación de la variable, haciéndola local para el shell actual.
- `-p`: Muestra todas las variables de entorno que están actualmente exportadas.

## Common Examples

### Exportar una variable
Para exportar una variable llamada `MY_VAR` con el valor `Hello`:

```bash
export MY_VAR="Hello"
```

### Verificar la variable exportada
Para verificar que la variable ha sido exportada, puedes usar el comando `echo`:

```bash
echo $MY_VAR
```

### Exportar múltiples variables
Puedes exportar múltiples variables en una sola línea:

```bash
export VAR1="Value1" VAR2="Value2"
```

### Eliminar la exportación de una variable
Si deseas que una variable deje de estar disponible para los procesos hijos, puedes usar la opción `-n`:

```bash
export -n MY_VAR
```

### Listar todas las variables exportadas
Para ver todas las variables de entorno que has exportado, utiliza:

```bash
export -p
```

## Tips
- Asegúrate de exportar las variables necesarias antes de ejecutar un script que dependa de ellas.
- Utiliza nombres de variables descriptivos para facilitar la comprensión del código.
- Recuerda que las variables exportadas solo estarán disponibles en el entorno de los procesos hijos, no en el shell padre.