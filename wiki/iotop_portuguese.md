# [Português] Debian Almquist Shell (dash) iotop Uso: Monitora o uso de I/O por processos

## Overview
O comando `iotop` é uma ferramenta útil para monitorar o uso de entrada/saída (I/O) em sistemas Linux. Ele exibe quais processos estão consumindo mais recursos de I/O, permitindo que os usuários identifiquem gargalos e otimizem o desempenho do sistema.

## Usage
A sintaxe básica do comando `iotop` é a seguinte:

```bash
iotop [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o `iotop`:

- `-o` ou `--only`: Mostra apenas os processos que estão realizando operações de I/O.
- `-b` ou `--batch`: Executa o `iotop` em modo batch, útil para redirecionar a saída para um arquivo.
- `-d <tempo>`: Define o intervalo de atualização em segundos.
- `-p <pid>`: Monitora apenas o processo com o ID especificado.

## Common Examples
Aqui estão alguns exemplos práticos de como usar o `iotop`:

1. **Executar o iotop em modo interativo**:
   ```bash
   iotop
   ```

2. **Mostrar apenas processos com atividade de I/O**:
   ```bash
   iotop -o
   ```

3. **Executar o iotop em modo batch e salvar a saída em um arquivo**:
   ```bash
   iotop -b -n 10 > iotop_output.txt
   ```

4. **Monitora um processo específico pelo seu PID**:
   ```bash
   iotop -p 1234
   ```

5. **Definir um intervalo de atualização de 2 segundos**:
   ```bash
   iotop -d 2
   ```

## Tips
- Utilize o modo `-o` para focar apenas nos processos que estão ativos, o que pode ajudar a identificar rapidamente os problemas de I/O.
- O modo batch é útil para registrar a atividade de I/O ao longo do tempo, permitindo uma análise posterior.
- Combine o `iotop` com outras ferramentas de monitoramento, como `top` ou `htop`, para obter uma visão mais abrangente do desempenho do sistema.