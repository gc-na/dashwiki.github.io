# [Português] Debian Almquist Shell (dash) grep Uso: Busca texto em arquivos

## Overview
O comando `grep` é utilizado para buscar padrões de texto em arquivos. Ele é uma ferramenta poderosa que permite filtrar linhas que correspondem a uma expressão regular, facilitando a localização de informações específicas em grandes volumes de dados.

## Usage
A sintaxe básica do comando `grep` é a seguinte:

```bash
grep [opções] [padrão] [arquivo]
```

## Common Options
Aqui estão algumas opções comuns do `grep`:

- `-i`: Ignora diferenças entre maiúsculas e minúsculas.
- `-v`: Inverte a correspondência, exibindo linhas que **não** correspondem ao padrão.
- `-r`: Realiza a busca recursivamente em diretórios.
- `-n`: Exibe o número da linha junto com a linha correspondente.
- `-l`: Lista apenas os nomes dos arquivos que contêm o padrão.

## Common Examples
Aqui estão alguns exemplos práticos do uso do `grep`:

1. **Buscar uma palavra em um arquivo:**
   ```bash
   grep "exemplo" arquivo.txt
   ```

2. **Buscar ignorando maiúsculas e minúsculas:**
   ```bash
   grep -i "exemplo" arquivo.txt
   ```

3. **Buscar recursivamente em um diretório:**
   ```bash
   grep -r "exemplo" /caminho/para/diretorio
   ```

4. **Exibir o número da linha com a correspondência:**
   ```bash
   grep -n "exemplo" arquivo.txt
   ```

5. **Listar arquivos que contêm a palavra:**
   ```bash
   grep -l "exemplo" *.txt
   ```

## Tips
- Utilize aspas ao redor do padrão de busca se ele contiver espaços ou caracteres especiais.
- Combine opções para refinar sua busca. Por exemplo, `grep -rin "exemplo" /caminho/para/diretorio` busca recursivamente, ignorando maiúsculas e minúsculas, e mostrando números de linha.
- Para padrões complexos, considere usar expressões regulares, que oferecem mais flexibilidade na busca.