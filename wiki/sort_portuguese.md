# [Português] Debian Almquist Shell (dash) sort uso equivalente: ordenar linhas de texto

## Overview
O comando `sort` é utilizado para ordenar linhas de texto em arquivos ou na entrada padrão. Ele organiza as linhas em ordem alfabética ou numérica, dependendo das opções utilizadas.

## Usage
A sintaxe básica do comando `sort` é a seguinte:

```bash
sort [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do comando `sort`:

- `-r`: Ordena as linhas em ordem reversa.
- `-n`: Ordena as linhas numericamente.
- `-k`: Especifica a coluna a ser usada para a ordenação.
- `-u`: Remove linhas duplicadas após a ordenação.
- `-o`: Especifica um arquivo de saída para os resultados ordenados.

## Common Examples

### Exemplo 1: Ordenar um arquivo
Para ordenar um arquivo chamado `lista.txt` em ordem alfabética, você pode usar:

```bash
sort lista.txt
```

### Exemplo 2: Ordenar em ordem reversa
Para ordenar o mesmo arquivo em ordem reversa, utilize a opção `-r`:

```bash
sort -r lista.txt
```

### Exemplo 3: Ordenar numericamente
Se você tiver um arquivo `numeros.txt` com números e quiser ordená-los numericamente, use:

```bash
sort -n numeros.txt
```

### Exemplo 4: Ordenar por coluna
Para ordenar um arquivo `dados.txt` pela segunda coluna, você pode usar:

```bash
sort -k2 dados.txt
```

### Exemplo 5: Remover duplicatas
Para ordenar um arquivo e remover linhas duplicadas, utilize a opção `-u`:

```bash
sort -u lista.txt
```

### Exemplo 6: Salvar a saída em um arquivo
Para salvar a saída ordenada em um novo arquivo `ordenado.txt`, use a opção `-o`:

```bash
sort -o ordenado.txt lista.txt
```

## Tips
- Sempre verifique o conteúdo do arquivo original antes de aplicar o comando `sort`, especialmente se você estiver usando a opção `-o`, pois ela sobrescreve o arquivo de saída.
- Combine opções para obter resultados mais específicos, como `sort -n -r` para ordenar números em ordem reversa.
- Utilize `man sort` no terminal para acessar a documentação completa e explorar mais opções disponíveis.