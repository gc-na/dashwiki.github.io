# [Português] Debian Almquist Shell (dash) xargs Uso: Executa comandos a partir da entrada padrão

## Overview
O comando `xargs` é utilizado para construir e executar comandos a partir da entrada padrão. Ele lê itens da entrada padrão e os utiliza como argumentos para um comando especificado, permitindo que você processe grandes quantidades de dados de forma eficiente.

## Usage
A sintaxe básica do comando `xargs` é a seguinte:

```bash
xargs [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do `xargs`:

- `-n N`: Especifica o número máximo de argumentos que serão passados para o comando por vez.
- `-d DELIM`: Define um delimitador personalizado para separar os itens da entrada.
- `-0`: Lê a entrada como uma lista de itens terminados por um caractere nulo (útil para nomes de arquivos que contêm espaços).
- `-p`: Pergunta ao usuário antes de executar cada comando.
- `-I {}`: Substitui `{}` pelo item lido da entrada.

## Common Examples

### Exemplo 1: Remover arquivos listados
Se você tiver uma lista de arquivos que deseja remover, pode usar `xargs` com o comando `rm`:

```bash
cat lista_de_arquivos.txt | xargs rm
```

### Exemplo 2: Contar palavras em arquivos
Para contar o número de palavras em todos os arquivos `.txt` em um diretório, você pode usar:

```bash
ls *.txt | xargs wc -w
```

### Exemplo 3: Usar um delimitador personalizado
Se você tiver uma lista de itens separados por vírgulas, pode usar o delimitador `-d`:

```bash
echo "item1,item2,item3" | xargs -d ',' echo
```

### Exemplo 4: Executar um comando com substituição
Você pode usar a opção `-I` para substituir um marcador em um comando:

```bash
echo "arquivo1 arquivo2" | xargs -I {} cp {} /destino/
```

## Tips
- Sempre verifique a entrada que você está passando para `xargs`, especialmente ao usar comandos destrutivos como `rm`.
- Use a opção `-p` para confirmar a execução de comandos potencialmente perigosos.
- Combine `xargs` com outros comandos como `find` para processar arquivos de maneira eficiente:

```bash
find . -name "*.log" | xargs rm
```