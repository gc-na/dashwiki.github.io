# [Português] Debian Almquist Shell (dash) dstat Uso equivalente: Monitora recursos do sistema em tempo real

## Overview
O comando `dstat` é uma ferramenta poderosa que permite monitorar em tempo real diversos recursos do sistema, como uso de CPU, memória, disco e rede. Ele combina funcionalidades de outras ferramentas, como `vmstat`, `iostat` e `netstat`, em uma única interface, facilitando a análise do desempenho do sistema.

## Usage
A sintaxe básica do comando `dstat` é a seguinte:

```bash
dstat [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do `dstat`:

- `-c`: Mostra o uso da CPU.
- `-d`: Exibe a atividade do disco.
- `-n`: Mostra a atividade da rede.
- `-m`: Exibe o uso da memória.
- `-t`: Adiciona um timestamp a cada linha de saída.
- `--help`: Mostra a ajuda e opções disponíveis.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `dstat`:

1. Para monitorar o uso da CPU e da memória:

   ```bash
   dstat -c -m
   ```

2. Para visualizar a atividade do disco e da rede:

   ```bash
   dstat -d -n
   ```

3. Para obter uma visão geral de todos os recursos com timestamps:

   ```bash
   dstat -t -c -d -n -m
   ```

4. Para monitorar o sistema por um período específico (por exemplo, 10 segundos):

   ```bash
   dstat 10
   ```

## Tips
- Utilize a opção `-t` para incluir timestamps, facilitando a correlação de eventos.
- Combine várias opções para obter uma visão mais abrangente do desempenho do sistema.
- Salve a saída do `dstat` em um arquivo para análise posterior, usando a redireção:

  ```bash
  dstat -c -d > dstat_output.txt
  ```

Essas práticas ajudarão a otimizar o uso do `dstat` e a obter informações valiosas sobre o desempenho do seu sistema.