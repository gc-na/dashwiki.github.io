# [Português] Debian Almquist Shell (dash) free: Exibir informações de memória

## Overview
O comando `free` é utilizado para exibir informações sobre a memória do sistema, incluindo a memória total, usada, livre e buffers/cache. É uma ferramenta útil para monitorar o uso de memória em tempo real.

## Usage
A sintaxe básica do comando `free` é a seguinte:

```bash
free [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do comando `free`:

- `-h`: Exibe os valores em um formato legível por humanos (por exemplo, em megabytes ou gigabytes).
- `-m`: Exibe a memória em megabytes.
- `-g`: Exibe a memória em gigabytes.
- `-s [intervalo]`: Atualiza a saída a cada intervalo de segundos.
- `-t`: Mostra a memória total, incluindo a memória usada e livre.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `free`:

1. Exibir informações de memória em um formato legível por humanos:

    ```bash
    free -h
    ```

2. Exibir a memória em megabytes:

    ```bash
    free -m
    ```

3. Exibir a memória em gigabytes:

    ```bash
    free -g
    ```

4. Atualizar a saída a cada 5 segundos:

    ```bash
    free -s 5
    ```

5. Exibir a memória total, incluindo a memória usada e livre:

    ```bash
    free -t
    ```

## Tips
- Utilize a opção `-h` para facilitar a leitura dos dados, especialmente em sistemas com grande quantidade de memória.
- Combine o comando `free` com outros comandos, como `watch`, para monitorar o uso de memória em tempo real. Por exemplo:

    ```bash
    watch free -h
    ```

- Fique atento ao uso de buffers/cache, pois isso pode afetar a interpretação da memória livre disponível.