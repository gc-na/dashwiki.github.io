# [Português] Debian Almquist Shell (dash) rmdir uso: Remove diretórios vazios

## Overview
O comando `rmdir` é utilizado para remover diretórios vazios no sistema de arquivos. Se o diretório contiver arquivos ou outros diretórios, o comando não será executado e retornará um erro.

## Usage
A sintaxe básica do comando `rmdir` é a seguinte:

```bash
rmdir [opções] [argumentos]
```

## Common Options
- `--ignore-fail-on-non-empty`: Ignora erros se o diretório não estiver vazio.
- `--parents`: Remove diretórios pai se eles estiverem vazios.
- `-p`: Sinônimo de `--parents`.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `rmdir`:

1. Remover um diretório vazio:
   ```bash
   rmdir meu_diretorio
   ```

2. Remover múltiplos diretórios vazios:
   ```bash
   rmdir dir1 dir2 dir3
   ```

3. Remover diretórios pai vazios:
   ```bash
   rmdir -p /caminho/para/diretorio/pai
   ```

4. Ignorar erros ao tentar remover um diretório não vazio:
   ```bash
   rmdir --ignore-fail-on-non-empty meu_diretorio
   ```

## Tips
- Sempre verifique se o diretório está realmente vazio antes de usar o `rmdir`, para evitar erros.
- Utilize o comando `ls` para listar o conteúdo do diretório antes de removê-lo.
- Considere usar `rmdir -p` para remover diretórios pai vazios em uma única operação, economizando tempo e esforço.