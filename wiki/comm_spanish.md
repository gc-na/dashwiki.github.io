# [Español] Debian Almquist Shell (dash) comm: Comparar líneas de archivos

## Overview
El comando `comm` se utiliza para comparar dos archivos de texto línea por línea. Este comando muestra las líneas que son únicas para cada archivo y las que son comunes entre ellos. Es especialmente útil para analizar diferencias entre listas o conjuntos de datos.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
comm [opciones] [archivo1] [archivo2]
```

## Common Options
- `-1`: Suprime las líneas que son únicas para el primer archivo.
- `-2`: Suprime las líneas que son únicas para el segundo archivo.
- `-3`: Suprime las líneas que son comunes a ambos archivos.
- `-i`: Ignora las diferencias entre mayúsculas y minúsculas al comparar las líneas.

## Common Examples

### Comparar dos archivos
Para comparar dos archivos y ver todas las líneas, puedes usar:

```bash
comm archivo1.txt archivo2.txt
```

### Suprimir líneas únicas del primer archivo
Si solo deseas ver las líneas que son comunes y las del segundo archivo, puedes usar:

```bash
comm -13 archivo1.txt archivo2.txt
```

### Ignorar mayúsculas y minúsculas
Para comparar dos archivos sin tener en cuenta las diferencias de mayúsculas y minúsculas:

```bash
comm -i archivo1.txt archivo2.txt
```

### Mostrar solo líneas únicas del segundo archivo
Si solo te interesan las líneas que son únicas para el segundo archivo:

```bash
comm -12 archivo1.txt archivo2.txt
```

## Tips
- Asegúrate de que los archivos estén ordenados antes de usar `comm`, ya que este comando requiere que las líneas de los archivos estén en orden alfabético.
- Puedes combinar `comm` con otros comandos como `sort` para procesar datos más complejos. Por ejemplo:

```bash
sort archivo1.txt | comm -12 - <(sort archivo2.txt)
```

- Utiliza las opciones adecuadas para filtrar la salida según tus necesidades, lo que puede hacer que la información sea más fácil de interpretar.