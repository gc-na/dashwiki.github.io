# [Português] Debian Almquist Shell (dash) uname Uso: Exibir informações do sistema

## Overview
O comando `uname` é utilizado para exibir informações sobre o sistema operacional em que o shell está sendo executado. Ele pode fornecer detalhes como o nome do kernel, a versão e outras informações relevantes.

## Usage
A sintaxe básica do comando `uname` é a seguinte:

```bash
uname [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do comando `uname`:

- `-a`: Exibe todas as informações disponíveis sobre o sistema.
- `-s`: Mostra o nome do kernel.
- `-n`: Exibe o nome do host da máquina.
- `-r`: Mostra a versão do kernel.
- `-v`: Exibe a data da versão do kernel.
- `-m`: Mostra a arquitetura da máquina.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `uname`:

1. Para exibir todas as informações do sistema:
   ```bash
   uname -a
   ```

2. Para mostrar apenas o nome do kernel:
   ```bash
   uname -s
   ```

3. Para obter a versão do kernel:
   ```bash
   uname -r
   ```

4. Para ver o nome do host da máquina:
   ```bash
   uname -n
   ```

5. Para verificar a arquitetura da máquina:
   ```bash
   uname -m
   ```

## Tips
- Utilize `uname -a` para obter uma visão geral completa do sistema em uma única linha.
- Combine `uname` com outros comandos, como `grep`, para filtrar informações específicas.
- Lembre-se de que as opções podem variar entre diferentes sistemas operacionais, então sempre consulte a documentação local se estiver em dúvida.