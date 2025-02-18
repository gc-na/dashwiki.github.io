# [Português] Debian Almquist Shell (dash) cmp Uso: Compara arquivos byte a byte

## Overview
O comando `cmp` é utilizado para comparar dois arquivos byte a byte. Ele é útil para identificar diferenças entre arquivos, especialmente em situações onde você precisa verificar se dois arquivos são idênticos ou não.

## Usage
A sintaxe básica do comando `cmp` é a seguinte:

```bash
cmp [opções] [arquivo1] [arquivo2]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o comando `cmp`:

- `-l`: Mostra as diferenças em formato octal.
- `-s`: Silencia a saída, retornando apenas o código de saída.
- `-i N`: Ignora os primeiros N bytes de cada arquivo.
- `-n N`: Compara apenas os primeiros N bytes dos arquivos.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `cmp`:

1. Comparar dois arquivos e exibir a primeira diferença encontrada:
   ```bash
   cmp arquivo1.txt arquivo2.txt
   ```

2. Comparar dois arquivos e mostrar as diferenças em formato octal:
   ```bash
   cmp -l arquivo1.bin arquivo2.bin
   ```

3. Comparar dois arquivos sem exibir a saída, apenas o código de saída:
   ```bash
   cmp -s arquivo1.txt arquivo2.txt
   ```

4. Comparar apenas os primeiros 100 bytes de dois arquivos:
   ```bash
   cmp -n 100 arquivo1.txt arquivo2.txt
   ```

5. Ignorar os primeiros 10 bytes de cada arquivo durante a comparação:
   ```bash
   cmp -i 10 arquivo1.txt arquivo2.txt
   ```

## Tips
- Use a opção `-s` se você estiver apenas interessado no resultado da comparação e não nas diferenças.
- Para arquivos binários, a opção `-l` pode ser muito útil para entender exatamente onde estão as diferenças.
- Lembre-se de que `cmp` para na primeira diferença encontrada; se você precisa comparar arquivos inteiros, considere usar `diff` para uma comparação mais detalhada.