# [Português] Debian Almquist Shell (dash) diff: Comparar arquivos linha a linha

## Overview
O comando `diff` é utilizado para comparar o conteúdo de dois arquivos, mostrando as diferenças entre eles. Ele é especialmente útil para desenvolvedores e administradores de sistema que precisam identificar alterações em arquivos de texto.

## Usage
A sintaxe básica do comando `diff` é a seguinte:

```bash
diff [opções] [arquivo1] [arquivo2]
```

## Common Options
Aqui estão algumas opções comuns do comando `diff`:

- `-u`: Exibe as diferenças em formato unificado, que é mais fácil de ler.
- `-c`: Mostra as diferenças em formato de contexto, incluindo algumas linhas de contexto ao redor das mudanças.
- `-i`: Ignora diferenças de maiúsculas e minúsculas.
- `-w`: Ignora espaços em branco ao comparar linhas.
- `-q`: Mostra apenas se os arquivos são diferentes, sem detalhar as diferenças.

## Common Examples

1. Comparar dois arquivos e exibir as diferenças:
   ```bash
   diff arquivo1.txt arquivo2.txt
   ```

2. Comparar arquivos com saída em formato unificado:
   ```bash
   diff -u arquivo1.txt arquivo2.txt
   ```

3. Ignorar diferenças de maiúsculas e minúsculas:
   ```bash
   diff -i arquivo1.txt arquivo2.txt
   ```

4. Comparar diretórios e listar arquivos que diferem:
   ```bash
   diff -rq diretorio1/ diretorio2/
   ```

5. Mostrar diferenças em formato de contexto:
   ```bash
   diff -c arquivo1.txt arquivo2.txt
   ```

## Tips
- Utilize a opção `-u` para facilitar a leitura das diferenças, especialmente em revisões de código.
- Combine opções como `-w` e `-i` para uma comparação mais flexível, ignorando espaços em branco e diferenças de capitalização.
- Para comparar diretórios, a opção `-r` é útil para verificar recursivamente todas as subpastas.