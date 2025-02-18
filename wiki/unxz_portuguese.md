# [Português] Debian Almquist Shell (dash) unxz Uso: Descompactar arquivos .xz

## Overview
O comando `unxz` é utilizado para descompactar arquivos que estão no formato `.xz`. Este formato é um método de compressão que oferece uma alta taxa de compressão, sendo bastante utilizado para reduzir o tamanho de arquivos em sistemas Unix e Linux.

## Usage
A sintaxe básica do comando `unxz` é a seguinte:

```bash
unxz [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o comando `unxz`:

- `-k`, `--keep`: Mantém o arquivo original após a descompressão.
- `-f`, `--force`: Força a descompressão, mesmo que o arquivo de saída já exista.
- `-v`, `--verbose`: Exibe informações detalhadas sobre o processo de descompressão.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `unxz`:

1. **Descompactar um arquivo .xz**:
   ```bash
   unxz arquivo.xz
   ```

2. **Descompactar e manter o arquivo original**:
   ```bash
   unxz -k arquivo.xz
   ```

3. **Forçar a descompressão de um arquivo existente**:
   ```bash
   unxz -f arquivo.xz
   ```

4. **Descompactar e exibir informações detalhadas**:
   ```bash
   unxz -v arquivo.xz
   ```

## Tips
- Sempre verifique se você tem espaço suficiente em disco antes de descompactar arquivos grandes.
- Use a opção `-k` se você quiser manter o arquivo original, especialmente se não tiver certeza se a descompressão será bem-sucedida.
- Para descompactar múltiplos arquivos de uma vez, você pode usar curingas, como `*.xz`, para descompactar todos os arquivos `.xz` em um diretório.