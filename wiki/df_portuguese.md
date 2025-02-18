# [Português] Debian Almquist Shell (dash) df Uso: Exibir informações sobre o uso do sistema de arquivos

## Overview
O comando `df` é utilizado para exibir informações sobre o espaço em disco disponível e utilizado em sistemas de arquivos montados. Ele fornece uma visão geral do uso do disco, permitindo que os usuários monitorem a capacidade de armazenamento de suas partições.

## Usage
A sintaxe básica do comando `df` é a seguinte:

```bash
df [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o comando `df`:

- `-h`: Exibe os tamanhos em um formato legível por humanos (por exemplo, KB, MB, GB).
- `-T`: Mostra o tipo de sistema de arquivos.
- `-a`: Inclui sistemas de arquivos que têm 0 blocos.
- `-i`: Exibe informações sobre inodes em vez de blocos.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `df`:

1. Exibir informações básicas sobre todos os sistemas de arquivos montados:
   ```bash
   df
   ```

2. Exibir informações em um formato legível por humanos:
   ```bash
   df -h
   ```

3. Mostrar o tipo de sistema de arquivos junto com as informações:
   ```bash
   df -T
   ```

4. Incluir sistemas de arquivos que têm 0 blocos:
   ```bash
   df -a
   ```

5. Exibir informações sobre inodes:
   ```bash
   df -i
   ```

## Tips
- Utilize a opção `-h` sempre que precisar de uma leitura rápida e fácil das informações de espaço em disco.
- Combine opções, como `df -hT`, para obter uma visão mais completa e legível dos sistemas de arquivos.
- Verifique regularmente o uso do disco para evitar problemas de espaço, especialmente em servidores e sistemas críticos.