# [Español] Debian Almquist Shell (dash) bg Uso equivalente en español: Mover trabajos a segundo plano

## Overview
El comando `bg` se utiliza en la shell para reanudar un trabajo detenido y moverlo al segundo plano. Esto permite que el usuario continúe utilizando la terminal mientras el trabajo sigue ejecutándose.

## Usage
La sintaxis básica del comando `bg` es la siguiente:

```bash
bg [opciones] [número del trabajo]
```

## Common Options
- `número del trabajo`: Especifica el trabajo que se desea mover al segundo plano. Si no se proporciona, `bg` reanuda el último trabajo detenido.

## Common Examples

1. **Reanudar el último trabajo detenido**:
   ```bash
   bg
   ```

2. **Reanudar un trabajo específico**:
   Supongamos que tienes un trabajo detenido con el número 1:
   ```bash
   bg %1
   ```

3. **Reanudar un trabajo específico con un comando**:
   Si tienes un trabajo que ejecutaste con un comando específico, puedes usar:
   ```bash
   bg %comando
   ```

## Tips
- Asegúrate de que el trabajo que deseas mover al segundo plano esté detenido. Puedes usar el comando `jobs` para ver el estado de los trabajos.
- Utiliza `fg` si necesitas llevar un trabajo del segundo plano de vuelta al primer plano.
- Recuerda que los trabajos en segundo plano seguirán ejecutándose incluso si cierras la terminal, a menos que se detengan o terminen.