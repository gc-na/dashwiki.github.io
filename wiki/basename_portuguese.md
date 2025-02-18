# [Português] Debian Almquist Shell (dash) basename uso equivalente: [remove o caminho e a extensão de um arquivo]

## Overview
O comando `basename` é utilizado para extrair o nome do arquivo de um caminho completo, removendo qualquer diretório e, opcionalmente, a extensão do arquivo. Isso é útil quando você precisa trabalhar apenas com o nome do arquivo sem a necessidade de seu caminho completo.

## Usage
A sintaxe básica do comando `basename` é a seguinte:

```bash
basename [opções] [argumentos]
```

## Common Options
- `-a`: Aceita múltiplos argumentos e retorna o nome base de cada um deles.
- `-s`: Remove a extensão especificada do nome do arquivo.
- `--help`: Exibe uma mensagem de ajuda com informações sobre o uso do comando.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `basename`:

1. **Extrair o nome do arquivo de um caminho completo:**
   ```bash
   basename /home/usuario/documentos/relatorio.txt
   ```
   Saída:
   ```
   relatorio.txt
   ```

2. **Remover a extensão de um arquivo:**
   ```bash
   basename /home/usuario/documentos/relatorio.txt .txt
   ```
   Saída:
   ```
   relatorio
   ```

3. **Usar a opção -a para múltiplos arquivos:**
   ```bash
   basename -a /home/usuario/imagens/foto1.jpg /home/usuario/imagens/foto2.png
   ```
   Saída:
   ```
   foto1.jpg
   foto2.png
   ```

4. **Remover a extensão de múltiplos arquivos:**
   ```bash
   basename -a /home/usuario/documentos/relatorio1.docx /home/usuario/documentos/relatorio2.docx .docx
   ```
   Saída:
   ```
   relatorio1
   relatorio2
   ```

## Tips
- Utilize `basename` em scripts para facilitar o processamento de arquivos, especialmente quando você precisa trabalhar apenas com os nomes.
- Combine `basename` com outros comandos, como `find`, para manipular arquivos de forma mais eficiente.
- Lembre-se de que o `basename` não altera os arquivos; ele apenas retorna o nome base, portanto, é seguro usá-lo em qualquer contexto.