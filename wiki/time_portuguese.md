# [Português] Debian Almquist Shell (dash) time <Uso equivalente em português>: [medir o tempo de execução de comandos]

## Overview
O comando `time` é utilizado para medir o tempo que um comando leva para ser executado. Ele fornece informações sobre o tempo real, o tempo de CPU e a memória utilizada durante a execução do comando.

## Usage
A sintaxe básica do comando `time` é a seguinte:

```bash
time [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do comando `time`:

- `-p`: Exibe o tempo em um formato mais legível, com os tempos separados por linhas.
- `-o <arquivo>`: Redireciona a saída do tempo para um arquivo especificado.
- `-f <formato>`: Permite personalizar a saída do tempo usando um formato específico.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `time`:

1. Medir o tempo de execução de um comando simples:
   ```bash
   time ls
   ```

2. Medir o tempo de execução de um script:
   ```bash
   time ./meu_script.sh
   ```

3. Usar a opção `-p` para um formato mais legível:
   ```bash
   time -p sleep 2
   ```

4. Redirecionar a saída do tempo para um arquivo:
   ```bash
   time -o tempo.txt sleep 3
   ```

5. Personalizar a saída do tempo:
   ```bash
   time -f "Tempo real: %e segundos" sleep 4
   ```

## Tips
- Utilize a opção `-p` para obter uma saída mais clara, especialmente se você estiver compartilhando os resultados com outras pessoas.
- Redirecionar a saída para um arquivo pode ser útil para registrar o desempenho de scripts ou comandos que você executa frequentemente.
- Experimente personalizar a saída com a opção `-f` para incluir apenas as informações que você considera mais relevantes.