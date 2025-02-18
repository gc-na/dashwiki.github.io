# [Português] Debian Almquist Shell (dash) expr Uso: Avaliar expressões

## Overview
O comando `expr` é utilizado para avaliar expressões aritméticas, lógicas e de string no shell. Ele permite realizar operações matemáticas simples, comparar valores e manipular strings, tornando-se uma ferramenta útil em scripts de shell.

## Usage
A sintaxe básica do comando `expr` é a seguinte:

```bash
expr [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do `expr`:

- `+` : Adição de dois números.
- `-` : Subtração de dois números.
- `*` : Multiplicação de dois números (deve ser escapado como `\*`).
- `/` : Divisão de dois números.
- `%` : Resto da divisão.
- `=` : Comparação de igualdade.
- `!=` : Comparação de desigualdade.
- `<` : Menor que.
- `>` : Maior que.
- `length` : Retorna o comprimento de uma string.

## Common Examples
Aqui estão alguns exemplos práticos do uso do `expr`:

### Exemplo 1: Adição de dois números
```bash
expr 5 + 3
```
Saída: `8`

### Exemplo 2: Subtração de dois números
```bash
expr 10 - 4
```
Saída: `6`

### Exemplo 3: Multiplicação de dois números
```bash
expr 4 \* 2
```
Saída: `8`

### Exemplo 4: Divisão de dois números
```bash
expr 20 / 4
```
Saída: `5`

### Exemplo 5: Comparação de igualdade
```bash
expr 5 = 5
```
Saída: `1` (verdadeiro)

### Exemplo 6: Comprimento de uma string
```bash
expr length "Olá, mundo!"
```
Saída: `12`

## Tips
- Sempre escape o asterisco (`*`) com uma barra invertida (`\`) para evitar que o shell o interprete como um caractere curinga.
- Utilize parênteses para agrupar expressões e controlar a ordem das operações.
- Para evitar problemas com espaços em branco, coloque as variáveis entre aspas ao usar `expr`.