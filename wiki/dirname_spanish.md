# [Español] Debian Almquist Shell (dash) dirname Uso: Extraer el nombre del directorio de una ruta

## Overview
El comando `dirname` se utiliza para extraer el nombre del directorio de una ruta de archivo. Esto es útil cuando se desea obtener la parte del directorio de una ruta completa, dejando de lado el nombre del archivo.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
dirname [opciones] [argumentos]
```

## Common Options
- `-z`: Trata los argumentos como cadenas nulas separadas por el carácter nulo en lugar de nuevas líneas.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `dirname`:

1. **Extraer el directorio de una ruta completa:**

```bash
dirname /home/usuario/documentos/archivo.txt
```
Salida:
```
/home/usuario/documentos
```

2. **Usar dirname con una ruta relativa:**

```bash
dirname ./proyectos/codigo.py
```
Salida:
```
./proyectos
```

3. **Obtener el directorio de un archivo en una ruta con espacios:**

```bash
dirname "/home/usuario/Mis Documentos/archivo.txt"
```
Salida:
```
/home/usuario/Mis Documentos
```

4. **Usar dirname en un script para procesar múltiples archivos:**

```bash
for file in /var/log/*.log; do
    echo "El directorio de $file es: $(dirname "$file")"
done
```

## Tips
- Siempre usa comillas alrededor de rutas que contengan espacios para evitar errores.
- Puedes combinar `dirname` con otros comandos como `find` o `xargs` para realizar operaciones más complejas sobre archivos y directorios.
- Recuerda que `dirname` solo devuelve el directorio; si necesitas el nombre del archivo, puedes usar el comando `basename`.