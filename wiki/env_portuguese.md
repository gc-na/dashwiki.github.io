# [Português] Debian Almquist Shell (dash) env: [executar comandos com variáveis de ambiente]

## Overview
O comando `env` é utilizado para executar um comando em um ambiente modificado, permitindo que você defina ou altere variáveis de ambiente temporariamente. Isso é útil para testar como um programa se comporta em diferentes configurações de ambiente.

## Usage
A sintaxe básica do comando `env` é a seguinte:

```bash
env [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do comando `env`:

- `-i`: Ignora o ambiente atual e executa o comando em um ambiente vazio.
- `-u VAR`: Remove a variável de ambiente especificada antes de executar o comando.
- `VAR=value`: Define uma variável de ambiente temporária para o comando a ser executado.

## Common Examples

### Executar um comando com variáveis de ambiente definidas
```bash
env VAR1=valor1 VAR2=valor2 comando
```
Neste exemplo, `VAR1` e `VAR2` são definidas apenas para a execução de `comando`.

### Ignorar o ambiente atual
```bash
env -i comando
```
Isso executa `comando` em um ambiente completamente vazio, sem nenhuma variável de ambiente pré-definida.

### Remover uma variável de ambiente
```bash
env -u PATH comando
```
Aqui, a variável `PATH` é removida antes da execução de `comando`.

## Tips
- Utilize `env` para testar scripts em diferentes ambientes sem alterar permanentemente as variáveis de ambiente do sistema.
- Combine `env` com outros comandos para criar ambientes de teste específicos.
- Lembre-se de que as variáveis definidas com `env` só estão disponíveis para o comando que você está executando e não afetam o ambiente global.