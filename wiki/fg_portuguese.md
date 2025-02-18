# [Português] Debian Almquist Shell (dash) fg <Uso equivalente em português>: Retornar um processo em segundo plano para o primeiro plano

## Overview
O comando `fg` é utilizado para trazer um processo que está em segundo plano de volta para o primeiro plano. Isso é útil quando você deseja interagir com um processo que foi pausado ou enviado para o fundo.

## Usage
A sintaxe básica do comando `fg` é a seguinte:

```bash
fg [opções] [número do trabalho]
```

## Common Options
- `número do trabalho`: Especifica qual trabalho em segundo plano você deseja trazer para o primeiro plano. Se não for especificado, o último trabalho em segundo plano será trazido.

## Common Examples

1. **Trazer o último trabalho em segundo plano para o primeiro plano:**
   ```bash
   fg
   ```

2. **Trazer um trabalho específico para o primeiro plano:**
   Suponha que você tenha dois trabalhos em segundo plano, e você deseja trazer o trabalho número 1:
   ```bash
   fg %1
   ```

3. **Trazer o trabalho número 2 para o primeiro plano:**
   ```bash
   fg %2
   ```

## Tips
- Use `jobs` antes de usar `fg` para listar todos os trabalhos em segundo plano e identificar o número do trabalho que você deseja trazer para o primeiro plano.
- Lembre-se de que, ao trazer um trabalho para o primeiro plano, você pode precisar interrompê-lo (Ctrl + C) se não quiser que ele continue executando.
- Se você deseja enviar um trabalho para o segundo plano novamente, pode usar o comando `bg` após usar `fg`.