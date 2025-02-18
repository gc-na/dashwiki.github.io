# [Português] Debian Almquist Shell (dash) printf uso: Formatar e imprimir texto

## Overview
O comando `printf` é utilizado para formatar e imprimir texto na saída padrão. Ele permite um controle preciso sobre a formatação, como a largura dos campos, a precisão dos números e a inclusão de caracteres especiais.

## Usage
A sintaxe básica do comando `printf` é a seguinte:

```sh
printf [opções] [formato] [argumentos...]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o comando `printf`:

- `-v var`: Armazena a saída em uma variável em vez de imprimi-la.
- `--help`: Mostra uma mensagem de ajuda com informações sobre o uso do comando.
- `--version`: Exibe a versão do comando.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `printf`:

1. **Imprimir uma string simples:**
   ```sh
   printf "Olá, mundo!\n"
   ```

2. **Formatar números:**
   ```sh
   printf "Número: %.2f\n" 3.14159
   ```

3. **Imprimir múltiplas variáveis:**
   ```sh
   nome="João"
   idade=30
   printf "Nome: %s, Idade: %d\n" "$nome" "$idade"
   ```

4. **Alinhar texto à direita:**
   ```sh
   printf "|%10s|\n" "Texto"
   ```

5. **Usar caracteres de escape:**
   ```sh
   printf "Linha 1\nLinha 2\n"
   ```

## Tips
- Utilize `%s` para strings, `%d` para inteiros e `%f` para números de ponto flutuante ao formatar a saída.
- Lembre-se de incluir `\n` no final de suas strings para garantir que a saída seja exibida corretamente em novas linhas.
- Teste suas formatações com diferentes entradas para garantir que a saída esteja conforme o esperado.