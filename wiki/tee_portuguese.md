# [Português] Debian Almquist Shell (dash) tee Uso: Redirecionar e gravar saída

## Overview
O comando `tee` é utilizado para ler da entrada padrão e gravar em um ou mais arquivos, além de exibir a saída no terminal. Isso permite que você visualize a saída de um comando enquanto também a salva em um arquivo.

## Usage
A sintaxe básica do comando `tee` é a seguinte:

```bash
tee [opções] [arquivos]
```

## Common Options
Aqui estão algumas opções comuns do comando `tee`:

- `-a`, `--append`: Adiciona a saída ao final do arquivo em vez de sobrescrevê-lo.
- `-i`, `--ignore-interrupts`: Ignora sinais de interrupção.
- `--help`: Exibe uma mensagem de ajuda com informações sobre o uso do comando.
- `--version`: Mostra a versão do comando `tee`.

## Common Examples

### Exemplo 1: Gravar a saída de um comando em um arquivo
```bash
echo "Olá, mundo!" | tee arquivo.txt
```
Este comando grava "Olá, mundo!" no arquivo `arquivo.txt` e também exibe a mensagem no terminal.

### Exemplo 2: Adicionar a saída a um arquivo existente
```bash
echo "Outra linha" | tee -a arquivo.txt
```
Aqui, "Outra linha" é adicionada ao final do `arquivo.txt`, mantendo o conteúdo anterior.

### Exemplo 3: Usar com múltiplos arquivos
```bash
echo "Texto para vários arquivos" | tee arquivo1.txt arquivo2.txt
```
Este comando grava "Texto para vários arquivos" em `arquivo1.txt` e `arquivo2.txt`, além de exibir a mensagem no terminal.

### Exemplo 4: Ignorar interrupções
```bash
some_command | tee -i arquivo.txt
```
Neste exemplo, `some_command` é executado e a saída é gravada em `arquivo.txt`, ignorando interrupções.

## Tips
- Utilize a opção `-a` quando quiser adicionar informações a um arquivo existente sem perder o conteúdo anterior.
- Combine `tee` com outros comandos usando pipes para capturar e registrar saídas de forma eficiente.
- Lembre-se de que o `tee` pode ser útil em scripts para registrar logs enquanto você ainda vê a saída no terminal.