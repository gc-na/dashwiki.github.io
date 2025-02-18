# [Português] Debian Almquist Shell (dash) pidstat Uso: Monitora estatísticas de processos

## Overview
O comando `pidstat` é uma ferramenta útil para monitorar estatísticas de uso de recursos de processos em sistemas Linux. Ele fornece informações detalhadas sobre a utilização de CPU, memória e outros recursos por processos individuais, permitindo que os usuários analisem o desempenho do sistema.

## Usage
A sintaxe básica do comando `pidstat` é a seguinte:

```bash
pidstat [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o `pidstat`:

- `-h`: Exibe a saída em um formato mais legível, com cabeçalhos.
- `-r`: Mostra informações sobre o uso de memória.
- `-u`: Exibe a utilização da CPU.
- `-p [PID]`: Monitora um processo específico pelo seu ID (PID).
- `-t`: Mostra estatísticas de threads.

## Common Examples

### Exibir uso de CPU de todos os processos
```bash
pidstat -u
```

### Monitorar um processo específico
```bash
pidstat -p 1234
```
(Substitua `1234` pelo PID do processo que você deseja monitorar.)

### Exibir uso de memória
```bash
pidstat -r
```

### Monitorar threads de um processo
```bash
pidstat -t -p 1234
```

### Exibir estatísticas a cada 2 segundos
```bash
pidstat 2
```

## Tips
- Utilize a opção `-h` para facilitar a leitura da saída, especialmente quando estiver analisando muitos processos.
- Combine opções para obter uma visão mais abrangente, como monitorar tanto a CPU quanto a memória de um processo específico.
- Para um monitoramento contínuo, considere usar `pidstat` em conjunto com outras ferramentas, como `watch`, para atualizar a saída em intervalos regulares.