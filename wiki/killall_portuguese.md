# [Português] Debian Almquist Shell (dash) killall Uso: Finaliza processos pelo nome

## Overview
O comando `killall` é utilizado para finalizar processos com base em seus nomes. Ele permite que os usuários encerrem múltiplos processos de uma só vez, tornando a gestão de tarefas mais eficiente.

## Usage
A sintaxe básica do comando `killall` é a seguinte:

```bash
killall [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do `killall`:

- `-s, --signal SIGNAL`: Especifica o sinal a ser enviado para os processos. O padrão é `TERM`.
- `-i, --interactive`: Solicita confirmação antes de encerrar cada processo.
- `-q, --quiet`: Não exibe mensagens de erro para processos que não foram encontrados.
- `-v, --verbose`: Exibe mensagens detalhadas sobre os processos que estão sendo encerrados.

## Common Examples
Aqui estão alguns exemplos práticos do uso do `killall`:

1. Para finalizar todos os processos com o nome "firefox":

    ```bash
    killall firefox
    ```

2. Para enviar um sinal específico, como `SIGKILL`, para todos os processos "gedit":

    ```bash
    killall -s KILL gedit
    ```

3. Para solicitar confirmação antes de encerrar cada processo "vlc":

    ```bash
    killall -i vlc
    ```

4. Para encerrar todos os processos "python" sem exibir mensagens de erro:

    ```bash
    killall -q python
    ```

5. Para exibir mensagens detalhadas ao encerrar processos "ssh":

    ```bash
    killall -v ssh
    ```

## Tips
- Sempre verifique quais processos estão em execução antes de usar `killall`, para evitar encerrar processos importantes acidentalmente.
- Use a opção `-i` se você não tiver certeza sobre quais processos estão sendo encerrados, pois isso ajuda a evitar erros.
- Combine `killall` com outros comandos, como `ps` ou `pgrep`, para identificar processos antes de encerrá-los.