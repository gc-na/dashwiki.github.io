# [Português] Debian Almquist Shell (dash) id uso: exibir informações do usuário

## Overview
O comando `id` é utilizado para exibir informações sobre o usuário atual ou sobre um usuário específico. Ele fornece detalhes como o UID (User ID), GID (Group ID) e os grupos aos quais o usuário pertence.

## Usage
A sintaxe básica do comando é a seguinte:

```bash
id [opções] [argumentos]
```

## Common Options
- `-u`: Exibe apenas o UID do usuário.
- `-g`: Exibe apenas o GID do grupo principal do usuário.
- `-G`: Exibe todos os GIDs dos grupos aos quais o usuário pertence.
- `-n`: Utilizado em conjunto com `-u` ou `-g`, exibe o nome em vez do número.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `id`:

1. Exibir informações do usuário atual:
   ```bash
   id
   ```

2. Exibir o UID do usuário atual:
   ```bash
   id -u
   ```

3. Exibir o GID do grupo principal do usuário atual:
   ```bash
   id -g
   ```

4. Exibir todos os GIDs dos grupos do usuário atual:
   ```bash
   id -G
   ```

5. Exibir informações de um usuário específico (por exemplo, "usuario"):
   ```bash
   id usuario
   ```

6. Exibir o nome do usuário atual em vez do UID:
   ```bash
   id -nu
   ```

## Tips
- Utilize `id` sem opções para obter uma visão geral rápida das informações do usuário.
- Combine as opções `-n` com `-u` ou `-g` para obter nomes legíveis em vez de números, facilitando a interpretação dos resultados.
- O comando `id` é útil para scripts que precisam verificar permissões ou grupos de usuários.