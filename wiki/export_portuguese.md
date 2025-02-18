# [Português] Debian Almquist Shell (dash) export uso: Define variáveis de ambiente

## Overview
O comando `export` no shell Debian Almquist (dash) é utilizado para definir variáveis de ambiente, tornando-as disponíveis para processos filhos. Isso é essencial para a configuração de ambientes de execução e para a passagem de informações entre scripts e programas.

## Usage
A sintaxe básica do comando `export` é a seguinte:

```sh
export [opções] [variável=valor]
```

## Common Options
- `-n`: Remove a variável do ambiente exportado.
- `-p`: Exibe todas as variáveis de ambiente que foram exportadas.

## Common Examples

### Exemplo 1: Exportar uma variável simples
```sh
export MY_VAR="Hello, World!"
```
Neste exemplo, a variável `MY_VAR` é definida e exportada com o valor "Hello, World!".

### Exemplo 2: Usar uma variável exportada em um comando
```sh
export USERNAME="usuario"
echo "O nome do usuário é $USERNAME"
```
Aqui, a variável `USERNAME` é exportada e utilizada em um comando `echo`.

### Exemplo 3: Remover uma variável do ambiente exportado
```sh
export -n MY_VAR
```
Este comando remove a variável `MY_VAR` do ambiente exportado, tornando-a não disponível para processos filhos.

### Exemplo 4: Listar todas as variáveis exportadas
```sh
export -p
```
Este comando exibe todas as variáveis que foram exportadas no ambiente atual.

## Tips
- Sempre que você definir uma variável que precisa ser acessada por outros scripts ou programas, use `export` para garantir que ela esteja disponível.
- Evite usar nomes de variáveis que possam conflitar com variáveis de sistema já existentes.
- Para verificar se uma variável foi exportada corretamente, você pode usar `printenv` ou `echo` para exibir seu valor.