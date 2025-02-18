# [Español] Debian Almquist Shell (dash) umask uso: Establecer permisos predeterminados para archivos y directorios

## Overview
El comando `umask` se utiliza en sistemas Unix y Linux para establecer la máscara de permisos predeterminados para nuevos archivos y directorios. Esta máscara determina qué permisos se quitarán de los permisos predeterminados que se asignan a los archivos y directorios cuando se crean.

## Usage
La sintaxis básica del comando `umask` es la siguiente:

```bash
umask [opciones] [argumentos]
```

## Common Options
- `-S`: Muestra la máscara de permisos en formato simbólico.
- `-p`: Muestra la máscara de permisos actual de manera persistente.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `umask`:

1. **Ver la máscara de permisos actual:**

   ```bash
   umask
   ```

2. **Establecer una nueva máscara de permisos:**

   ```bash
   umask 027
   ```

   Esto establece que los nuevos archivos tendrán permisos `rw-r-----` y los nuevos directorios `rwxr-x---`.

3. **Ver la máscara de permisos en formato simbólico:**

   ```bash
   umask -S
   ```

4. **Restablecer la máscara de permisos a su valor predeterminado:**

   ```bash
   umask 002
   ```

## Tips
- Recuerda que la máscara de permisos se aplica solo a los archivos y directorios nuevos; no afecta a los existentes.
- Puedes agregar el comando `umask` a tu archivo de inicio (como `.bashrc` o `.profile`) para establecer una máscara de permisos predeterminada cada vez que inicies sesión.
- Ten cuidado al establecer una máscara demasiado restrictiva, ya que puede dificultar el acceso a los archivos por parte de otros usuarios.