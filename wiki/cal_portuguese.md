# [Português] Debian Almquist Shell (dash) cal: Exibir um calendário

## Overview
O comando `cal` é utilizado para exibir um calendário no terminal. Ele pode mostrar o calendário de um mês específico, de um ano inteiro ou até mesmo de um intervalo de meses, dependendo das opções utilizadas.

## Usage
A sintaxe básica do comando é a seguinte:

```bash
cal [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o comando `cal`:

- `-m`: Exibe o calendário começando pela segunda-feira.
- `-y`: Mostra o calendário do ano atual.
- `-3`: Exibe o calendário do mês atual, do mês anterior e do próximo mês.
- `-j`: Mostra o calendário com números de dias julianos.

## Common Examples
Aqui estão alguns exemplos práticos de como usar o comando `cal`:

1. Exibir o calendário do mês atual:
   ```bash
   cal
   ```

2. Exibir o calendário de um mês específico (por exemplo, janeiro de 2023):
   ```bash
   cal 01 2023
   ```

3. Exibir o calendário do ano atual:
   ```bash
   cal -y
   ```

4. Exibir o calendário do mês atual, do mês anterior e do próximo mês:
   ```bash
   cal -3
   ```

5. Exibir o calendário de um ano específico (por exemplo, 2023):
   ```bash
   cal 2023
   ```

6. Exibir o calendário com números de dias julianos:
   ```bash
   cal -j
   ```

## Tips
- Utilize a opção `-m` se você preferir que a semana comece na segunda-feira, em vez do domingo.
- Combine o `cal` com outros comandos, como `grep`, para encontrar datas específicas ou eventos.
- Experimente usar `cal` em scripts para gerar relatórios ou lembretes de datas importantes.