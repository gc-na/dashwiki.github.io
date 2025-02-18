# [Português] Debian Almquist Shell (dash) head <Uso equivalente em português>: exibir as primeiras linhas de um arquivo

## Overview
O comando `head` é utilizado para exibir as primeiras linhas de um arquivo de texto. Por padrão, ele mostra as primeiras 10 linhas, mas esse número pode ser ajustado conforme necessário.

## Usage
A sintaxe básica do comando `head` é a seguinte:

```bash
head [opções] [arquivos]
```

## Common Options
Aqui estão algumas opções comuns do comando `head`:

- `-n [número]`: Especifica o número de linhas a serem exibidas. Por exemplo, `-n 5` exibirá as primeiras 5 linhas.
- `-c [número]`: Exibe os primeiros bytes do arquivo. Por exemplo, `-c 100` mostrará os primeiros 100 bytes.
- `-q`: Suprime a impressão do cabeçalho dos arquivos quando múltiplos arquivos são fornecidos.
- `-v`: Sempre imprime o cabeçalho dos arquivos, mesmo que apenas um arquivo seja fornecido.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `head`:

1. Exibir as primeiras 10 linhas de um arquivo chamado `exemplo.txt`:

   ```bash
   head exemplo.txt
   ```

2. Exibir as primeiras 5 linhas de um arquivo:

   ```bash
   head -n 5 exemplo.txt
   ```

3. Exibir os primeiros 100 bytes de um arquivo:

   ```bash
   head -c 100 exemplo.txt
   ```

4. Exibir as primeiras 10 linhas de múltiplos arquivos:

   ```bash
   head arquivo1.txt arquivo2.txt
   ```

5. Exibir as primeiras 3 linhas de um arquivo e mostrar o cabeçalho:

   ```bash
   head -v -n 3 exemplo.txt
   ```

## Tips
- Use o comando `head` em conjunto com outros comandos, como `grep`, para filtrar e visualizar rapidamente as primeiras linhas de resultados.
- Para visualizar as primeiras linhas de saída de um comando, você pode usar o pipe. Por exemplo:

  ```bash
  ls -l | head -n 5
  ```

- Lembre-se de que o `head` é útil para verificar rapidamente o conteúdo de arquivos grandes sem precisar abri-los completamente.