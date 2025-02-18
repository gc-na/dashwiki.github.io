# [Português] Debian Almquist Shell (dash) du <Uso equivalente em português>: Exibir o uso de espaço em disco

## Overview
O comando `du` (disk usage) é utilizado para estimar e exibir o espaço em disco utilizado por arquivos e diretórios. Ele é especialmente útil para identificar quais arquivos ou diretórios estão consumindo mais espaço em um sistema.

## Usage
A sintaxe básica do comando `du` é a seguinte:

```bash
du [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do comando `du`:

- `-h`: Exibe os tamanhos em um formato legível por humanos (por exemplo, KB, MB).
- `-s`: Mostra apenas o total para cada argumento, sem listar subdiretórios.
- `-a`: Inclui arquivos individuais na saída, além de diretórios.
- `-c`: Exibe um total acumulado no final da saída.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `du`:

1. Exibir o uso de espaço em disco de um diretório específico em um formato legível:
   ```bash
   du -h /caminho/para/diretorio
   ```

2. Mostrar o total de espaço utilizado por um diretório, sem listar subdiretórios:
   ```bash
   du -sh /caminho/para/diretorio
   ```

3. Listar o uso de espaço de todos os arquivos e diretórios no diretório atual:
   ```bash
   du -ah .
   ```

4. Exibir o uso de espaço em disco e incluir um total acumulado:
   ```bash
   du -ch /caminho/para/diretorio
   ```

## Tips
- Utilize a opção `-h` para facilitar a leitura dos tamanhos, especialmente em diretórios grandes.
- Combine `du` com outros comandos, como `sort`, para classificar os diretórios pelo tamanho:
  ```bash
  du -h /caminho/para/diretorio | sort -hr
  ```
- Verifique o uso de espaço em diretórios temporários ou de cache para liberar espaço em disco.