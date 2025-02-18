# [Português] Debian Almquist Shell (dash) dirname Uso: Extrair o diretório de um caminho

## Overview
O comando `dirname` é utilizado para extrair o caminho do diretório de um arquivo ou caminho especificado. Ele remove o nome do arquivo e retorna apenas a parte do diretório.

## Usage
A sintaxe básica do comando `dirname` é a seguinte:

```bash
dirname [caminho]
```

## Common Options
O comando `dirname` não possui muitas opções, mas aqui estão algumas comuns:

- `-z`: Trata os caminhos como terminados por nulo, útil para trabalhar com listas de arquivos.

## Common Examples

### Exemplo 1: Extrair o diretório de um caminho simples
```bash
dirname /home/usuario/documento.txt
```
**Saída:**
```
/home/usuario
```

### Exemplo 2: Usar com um caminho relativo
```bash
dirname ./imagens/foto.jpg
```
**Saída:**
```
./imagens
```

### Exemplo 3: Extrair o diretório de um caminho com múltiplos níveis
```bash
dirname /var/log/syslog
```
**Saída:**
```
/var/log
```

### Exemplo 4: Usar com um caminho terminado em barra
```bash
dirname /usr/local/bin/
```
**Saída:**
```
/usr/local/bin
```

## Tips
- Utilize `dirname` em scripts para manipular caminhos de arquivos de forma eficiente.
- Combine `dirname` com outros comandos, como `basename`, para obter tanto o diretório quanto o nome do arquivo.
- Lembre-se de que `dirname` não altera o sistema de arquivos; ele apenas fornece uma representação do caminho.