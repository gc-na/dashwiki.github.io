# [Português] Debian Almquist Shell (dash) strace uso: rastrear chamadas de sistema

## Overview
O comando `strace` é uma ferramenta poderosa que permite rastrear as chamadas de sistema e sinais recebidos por um processo em execução. Ele é útil para depuração e análise de desempenho, pois fornece informações detalhadas sobre como um programa interage com o sistema operacional.

## Usage
A sintaxe básica do comando `strace` é a seguinte:

```bash
strace [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do `strace`:

- `-o <arquivo>`: Redireciona a saída do `strace` para um arquivo em vez de exibi-la no terminal.
- `-e <expressão>`: Filtra as chamadas de sistema para incluir apenas aquelas que correspondem à expressão especificada.
- `-p <PID>`: Anexa o `strace` a um processo em execução, identificado pelo seu ID de processo (PID).
- `-c`: Resumidamente conta as chamadas de sistema e exibe estatísticas ao final da execução.
- `-f`: Segue processos filhos criados por chamadas de fork.

## Common Examples
Aqui estão alguns exemplos práticos do uso do `strace`:

1. Rastrear um comando simples e exibir a saída no terminal:
   ```bash
   strace ls
   ```

2. Rastrear um comando e salvar a saída em um arquivo:
   ```bash
   strace -o output.txt ls
   ```

3. Anexar o `strace` a um processo em execução:
   ```bash
   strace -p 1234
   ```

4. Filtrar chamadas de sistema específicas, como `open`:
   ```bash
   strace -e trace=open ls
   ```

5. Contar chamadas de sistema e exibir estatísticas:
   ```bash
   strace -c ls
   ```

## Tips
- Use a opção `-o` para salvar a saída em um arquivo, facilitando a análise posterior.
- Combine `strace` com outras ferramentas, como `grep`, para filtrar a saída em tempo real.
- Sempre verifique o PID do processo antes de usar a opção `-p` para evitar anexar-se ao processo errado.
- Lembre-se de que o uso do `strace` pode impactar o desempenho do programa rastreado, especialmente em aplicações que fazem muitas chamadas de sistema.