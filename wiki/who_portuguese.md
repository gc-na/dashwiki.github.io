# [Português] Debian Almquist Shell (dash) who: exibe usuários logados

## Overview
O comando `who` é utilizado para exibir uma lista de usuários que estão atualmente logados no sistema. Ele fornece informações sobre os usuários, como o nome de usuário, o terminal em que estão logados, a data e hora do login, entre outros detalhes.

## Usage
A sintaxe básica do comando `who` é a seguinte:

```bash
who [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do comando `who`:

- `-b`: Exibe a hora da última inicialização do sistema.
- `-q`: Mostra uma lista de usuários logados e a contagem total de usuários.
- `-H`: Exibe os cabeçalhos das colunas na saída.

## Common Examples

### Exibir usuários logados
Para ver todos os usuários que estão logados no sistema, você pode usar:

```bash
who
```

### Exibir a hora da última inicialização
Para verificar quando o sistema foi iniciado pela última vez, utilize a opção `-b`:

```bash
who -b
```

### Contar usuários logados
Se você deseja apenas saber quantos usuários estão logados, use a opção `-q`:

```bash
who -q
```

### Exibir cabeçalhos das colunas
Para incluir cabeçalhos na saída do comando, utilize a opção `-H`:

```bash
who -H
```

## Tips
- Utilize `who` em conjunto com outros comandos, como `grep`, para filtrar informações específicas sobre usuários.
- Lembre-se de que o comando `who` pode não mostrar usuários que estão logados via SSH se você não tiver permissões adequadas.
- Para uma visão mais detalhada, considere usar o comando `w`, que fornece informações adicionais sobre a atividade dos usuários logados.