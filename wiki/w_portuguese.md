# [Debian] Debian Almquist Shell (dash) w: [exibir usuários conectados]

## Overview
O comando `w` é utilizado para exibir informações sobre os usuários que estão atualmente conectados ao sistema, bem como suas atividades. Ele fornece detalhes como o tempo de atividade do sistema, o tempo que cada usuário está logado, e o que cada um deles está fazendo no momento.

## Usage
A sintaxe básica do comando `w` é a seguinte:

```bash
w [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o comando `w`:

- `-h`: Não exibe o cabeçalho da tabela.
- `-s`: Exibe a saída em um formato mais compacto.
- `-u`: Exibe o nome do usuário em vez do ID do usuário.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `w`:

1. Exibir todos os usuários conectados e suas atividades:
   ```bash
   w
   ```

2. Exibir a lista de usuários sem o cabeçalho:
   ```bash
   w -h
   ```

3. Exibir a lista de usuários em um formato compacto:
   ```bash
   w -s
   ```

4. Exibir informações de um usuário específico:
   ```bash
   w nome_do_usuario
   ```

## Tips
- Utilize o comando `w` regularmente para monitorar a atividade dos usuários em sistemas multiusuário.
- Combine o `w` com outros comandos, como `grep`, para filtrar informações específicas.
- Familiarize-se com as opções disponíveis para personalizar a saída de acordo com suas necessidades.