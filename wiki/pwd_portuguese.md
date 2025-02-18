# [Português] Debian Almquist Shell (dash) pwd Uso equivalente: Exibir o diretório de trabalho atual

## Overview
O comando `pwd` (print working directory) é utilizado para exibir o caminho completo do diretório de trabalho atual em que o usuário se encontra no sistema de arquivos. É uma ferramenta simples, mas essencial para navegação e gerenciamento de arquivos no terminal.

## Usage
A sintaxe básica do comando `pwd` é a seguinte:

```bash
pwd [opções]
```

## Common Options
O comando `pwd` possui algumas opções comuns que podem ser utilizadas:

- `-L`: Exibe o caminho lógico do diretório atual, que pode incluir links simbólicos.
- `-P`: Exibe o caminho físico do diretório atual, resolvendo todos os links simbólicos.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `pwd`:

1. Exibir o diretório de trabalho atual:
   ```bash
   pwd
   ```

2. Exibir o caminho lógico do diretório atual:
   ```bash
   pwd -L
   ```

3. Exibir o caminho físico do diretório atual:
   ```bash
   pwd -P
   ```

## Tips
- Utilize `pwd` frequentemente para confirmar sua localização no sistema de arquivos, especialmente antes de executar comandos que afetam arquivos ou diretórios.
- Combine o uso de `pwd` com outros comandos, como `cd`, para uma navegação mais eficiente.
- Lembre-se de que o comando `pwd` é útil em scripts para verificar o diretório atual antes de realizar operações de arquivo.