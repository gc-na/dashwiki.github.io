# [Português] Debian Almquist Shell (dash) bg: Colocar processos em segundo plano

## Overview
O comando `bg` é utilizado no shell para retomar a execução de processos que estão suspensos, colocando-os em segundo plano. Isso permite que o usuário continue usando o terminal enquanto o processo é executado.

## Usage
A sintaxe básica do comando `bg` é a seguinte:

```bash
bg [opções] [número do trabalho]
```

## Common Options
- **`%n`**: Especifica o trabalho a ser colocado em segundo plano, onde `n` é o número do trabalho.
- **`-`**: Retoma o último trabalho suspenso.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `bg`:

1. Colocar o último trabalho suspenso em segundo plano:
   ```bash
   bg
   ```

2. Colocar um trabalho específico em segundo plano usando seu número:
   ```bash
   bg %1
   ```

3. Colocar um trabalho em segundo plano e continuar a execução:
   ```bash
   sleep 100 &
   # Após suspender o trabalho com Ctrl+Z, use:
   bg %1
   ```

## Tips
- Sempre verifique a lista de trabalhos suspensos com o comando `jobs` antes de usar `bg`, para saber qual trabalho você deseja retomar.
- Use `fg` se você quiser trazer um trabalho de volta para o primeiro plano.
- Lembre-se de que processos em segundo plano podem gerar saída no terminal, então esteja ciente de como isso pode afetar sua experiência de uso.