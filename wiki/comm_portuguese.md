# [Português] Debian Almquist Shell (dash) comm: Compara duas listas de arquivos

## Overview
O comando `comm` é utilizado para comparar duas listas de arquivos ordenadas linha por linha. Ele exibe as linhas que são exclusivas a cada arquivo, bem como as linhas que são comuns a ambos.

## Usage
A sintaxe básica do comando é a seguinte:

```bash
comm [opções] [arquivo1] [arquivo2]
```

## Common Options
- `-1`: Suprime a saída das linhas que estão apenas no primeiro arquivo.
- `-2`: Suprime a saída das linhas que estão apenas no segundo arquivo.
- `-3`: Suprime a saída das linhas que estão em ambos os arquivos.
- `--nocheck-order`: Permite que os arquivos não estejam ordenados.

## Common Examples

### Exemplo 1: Comparar duas listas
Para comparar duas listas de nomes em arquivos diferentes:

```bash
comm lista1.txt lista2.txt
```

### Exemplo 2: Exibir apenas linhas exclusivas do segundo arquivo
Para mostrar apenas as linhas que estão no segundo arquivo e não no primeiro:

```bash
comm -13 lista1.txt lista2.txt
```

### Exemplo 3: Exibir apenas linhas comuns
Para exibir somente as linhas que aparecem em ambos os arquivos:

```bash
comm -12 lista1.txt lista2.txt
```

### Exemplo 4: Comparar arquivos não ordenados
Se os arquivos não estiverem ordenados, você pode usar a opção `--nocheck-order`:

```bash
comm --nocheck-order arquivo1.txt arquivo2.txt
```

## Tips
- Certifique-se de que os arquivos estejam ordenados antes de usar o `comm`, a menos que você utilize a opção `--nocheck-order`.
- Utilize redirecionamento para salvar a saída do comando em um novo arquivo, se necessário:

```bash
comm lista1.txt lista2.txt > resultado.txt
```
- Combine o `comm` com outros comandos, como `sort`, para garantir que os arquivos estejam ordenados:

```bash
comm <(sort lista1.txt) <(sort lista2.txt)
```