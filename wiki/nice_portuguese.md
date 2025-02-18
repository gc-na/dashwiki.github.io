# [Português] Debian Almquist Shell (dash) nice uso equivalente: Ajusta a prioridade de execução de processos

## Overview
O comando `nice` é utilizado para executar um programa com uma prioridade de CPU ajustada. Isso permite que você controle a quantidade de recursos do sistema que um processo pode consumir, ajudando a evitar que processos intensivos em CPU afetem o desempenho de outros processos.

## Usage
A sintaxe básica do comando `nice` é a seguinte:

```bash
nice [opções] [comando]
```

## Common Options
Aqui estão algumas opções comuns do comando `nice`:

- `-n, --adjustment=N`: Define o valor de ajuste da prioridade. O valor padrão é 10, e o intervalo varia de -20 (máxima prioridade) a 19 (mínima prioridade).
- `--help`: Exibe uma mensagem de ajuda com informações sobre o uso do comando.
- `--version`: Mostra a versão do comando `nice`.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `nice`:

1. Executar um script com prioridade padrão:
   ```bash
   nice ./meu_script.sh
   ```

2. Executar um comando com prioridade reduzida:
   ```bash
   nice -n 10 ./meu_programa
   ```

3. Executar um comando com prioridade aumentada:
   ```bash
   nice -n -5 ./meu_programa
   ```

4. Verificar a prioridade de um processo em execução:
   ```bash
   ps -o pid,nice,cmd
   ```

## Tips
- Use valores negativos com cuidado, pois eles aumentam a prioridade do processo e podem impactar negativamente outros processos no sistema.
- Para verificar a prioridade de um processo em execução, você pode usar o comando `ps` junto com a opção `-o` para exibir a coluna de prioridade.
- Combine o `nice` com outros comandos, como `nohup`, para executar processos em segundo plano sem se preocupar com a sessão do terminal.