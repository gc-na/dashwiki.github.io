# [Português] Debian Almquist Shell (dash) top uso: Monitore o uso de recursos do sistema

## Overview
O comando `top` é uma ferramenta poderosa que permite monitorar em tempo real o uso de recursos do sistema, como CPU e memória. Ele exibe uma lista de processos em execução, permitindo que os usuários vejam quais estão consumindo mais recursos.

## Usage
A sintaxe básica do comando `top` é a seguinte:

```bash
top [opções]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o comando `top`:

- `-d <segundos>`: Define o intervalo de atualização em segundos.
- `-n <número>`: Especifica o número de iterações que o `top` deve executar antes de sair.
- `-b`: Executa o `top` em modo batch, útil para redirecionar a saída para um arquivo.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `top`:

1. Executar o `top` com a atualização padrão:
   ```bash
   top
   ```

2. Executar o `top` com um intervalo de atualização de 2 segundos:
   ```bash
   top -d 2
   ```

3. Executar o `top` em modo batch e salvar a saída em um arquivo:
   ```bash
   top -b -n 1 > top_output.txt
   ```

4. Limitar a execução do `top` a 5 iterações:
   ```bash
   top -n 5
   ```

## Tips
- Para sair do `top`, pressione `q`.
- Você pode ordenar os processos por diferentes critérios, como uso de CPU ou memória, pressionando as teclas correspondentes enquanto o `top` está em execução.
- Utilize a tecla `h` para acessar a ajuda dentro do `top` e descobrir mais sobre suas funcionalidades.