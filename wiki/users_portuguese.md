# [Português] Usuários do Debian Almquist Shell (dash): exibir informações sobre usuários do sistema

## Overview
O comando `users` é utilizado para exibir os nomes dos usuários que estão atualmente logados no sistema. Ele fornece uma visão rápida de quem está ativo no momento, o que pode ser útil para administração de sistemas e monitoramento.

## Usage
A sintaxe básica do comando é a seguinte:

```bash
users [opções]
```

## Common Options
O comando `users` não possui muitas opções, mas aqui estão algumas que podem ser úteis:

- `-n`: Exibe o número de usuários logados em vez de seus nomes.
- `-r`: Exibe apenas os usuários que estão logados em sessões reais (exclui usuários que estão logados via serviços como SSH, mas não têm sessões ativas).

## Common Examples

Aqui estão alguns exemplos práticos do uso do comando `users`:

1. **Exibir usuários logados:**
   ```bash
   users
   ```

2. **Contar o número de usuários logados:**
   ```bash
   users -n
   ```

3. **Exibir apenas usuários com sessões reais:**
   ```bash
   users -r
   ```

## Tips
- Utilize o comando `who` se precisar de informações mais detalhadas sobre os usuários logados, como o terminal que estão usando e a hora do login.
- Combine o comando `users` com outros comandos, como `wc -w`, para contar quantos usuários estão logados:
  ```bash
  users | wc -w
  ```
- Lembre-se de que o comando `users` exibe os nomes dos usuários em uma única linha, separados por espaços, o que pode ser útil para scripts que precisam processar essa informação.