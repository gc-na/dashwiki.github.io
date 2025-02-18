# [Português] Debian Almquist Shell (dash) trap uso: Captura de sinais e execução de comandos

## Overview
O comando `trap` no shell Debian Almquist (dash) é utilizado para capturar sinais e executar comandos específicos quando esses sinais são recebidos. Isso é útil para gerenciar o comportamento de scripts em resposta a eventos como interrupções do usuário ou finalizações de processos.

## Usage
A sintaxe básica do comando `trap` é a seguinte:

```sh
trap [opções] [comando] [sinal]
```

## Common Options
Aqui estão algumas opções comuns do comando `trap`:

- `-p`: Exibe as configurações atuais do `trap`.
- `-l`: Lista todos os sinais disponíveis que podem ser capturados.

## Common Examples

### Exemplo 1: Capturando a interrupção do usuário
Este exemplo mostra como capturar a interrupção (Ctrl+C) e executar um comando específico:

```sh
trap 'echo "Interrupção recebida!"' SIGINT
while true; do
    echo "Executando... Pressione Ctrl+C para interromper."
    sleep 1
done
```

### Exemplo 2: Limpeza antes de sair
Neste exemplo, o comando `trap` é usado para garantir que um diretório temporário seja removido quando o script é encerrado:

```sh
trap 'rm -rf /tmp/meu_diretorio_temp' EXIT
mkdir /tmp/meu_diretorio_temp
echo "Diretório temporário criado. Pressione Ctrl+C para sair."
sleep 10
```

### Exemplo 3: Capturando vários sinais
Você pode capturar múltiplos sinais e executar comandos diferentes para cada um:

```sh
trap 'echo "Sinal SIGTERM recebido!"' SIGTERM
trap 'echo "Sinal SIGQUIT recebido!"' SIGQUIT
while true; do
    echo "Executando... Pressione Ctrl+\ para enviar SIGQUIT ou use kill para enviar SIGTERM."
    sleep 1
done
```

## Tips
- Sempre teste seu script para garantir que os comandos no `trap` sejam executados conforme esperado.
- Use `trap` para realizar tarefas de limpeza, como remover arquivos temporários ou liberar recursos, ao sair de um script.
- Lembre-se de que os sinais podem ser enviados de várias maneiras, então considere quais sinais são mais relevantes para o seu script.