# [Português] Debian Almquist Shell (dash) uniq Uso: Remove linhas duplicadas de um arquivo

## Overview
O comando `uniq` é utilizado para filtrar linhas duplicadas em um arquivo ou na entrada padrão. Ele compara linhas adjacentes e remove as duplicatas, exibindo apenas uma ocorrência de cada linha.

## Usage
A sintaxe básica do comando `uniq` é a seguinte:

```bash
uniq [opções] [arquivos]
```

## Common Options
Aqui estão algumas opções comuns do `uniq`:

- `-c`: Conta o número de ocorrências de cada linha.
- `-d`: Exibe apenas as linhas que são duplicadas.
- `-u`: Exibe apenas as linhas que são únicas (não duplicadas).
- `-i`: Ignora diferenças entre maiúsculas e minúsculas ao comparar linhas.

## Common Examples

1. **Remover duplicatas de um arquivo:**

```bash
uniq arquivo.txt
```

2. **Contar o número de ocorrências de cada linha:**

```bash
uniq -c arquivo.txt
```

3. **Exibir apenas linhas duplicadas:**

```bash
uniq -d arquivo.txt
```

4. **Exibir apenas linhas únicas:**

```bash
uniq -u arquivo.txt
```

5. **Ignorar diferenças de maiúsculas e minúsculas:**

```bash
uniq -i arquivo.txt
```

## Tips
- Para que o `uniq` funcione corretamente, as linhas duplicadas devem estar adjacentes. Use o comando `sort` antes de `uniq` para garantir que as duplicatas sejam agrupadas.
- Combine opções para personalizar a saída, como `sort arquivo.txt | uniq -c` para contar as ocorrências de cada linha após a ordenação.
- Verifique sempre a entrada do arquivo para garantir que não haja espaços em branco ou caracteres ocultos que possam afetar a comparação.