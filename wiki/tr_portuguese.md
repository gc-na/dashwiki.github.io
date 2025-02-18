# [Português] Debian Almquist Shell (dash) tr <Uso equivalente em português>: substituir ou remover caracteres

## Overview
O comando `tr` é utilizado para traduzir ou remover caracteres de uma entrada. Ele lê da entrada padrão e pode ser usado para modificar texto de forma simples e eficaz.

## Usage
A sintaxe básica do comando `tr` é a seguinte:

```bash
tr [opções] [argumentos]
```

## Common Options
- `-d`: Remove caracteres especificados.
- `-s`: Substitui sequências de caracteres repetidos por um único caractere.
- `-c`: Complementa o conjunto de caracteres especificados.

## Common Examples

1. **Substituir caracteres**:
   Para substituir todas as letras minúsculas 'a' por letras maiúsculas 'A':
   ```bash
   echo "banana" | tr 'a' 'A'
   ```

2. **Remover caracteres**:
   Para remover todas as vogais de uma string:
   ```bash
   echo "Olá, mundo!" | tr -d 'aeiouáéíóú'
   ```

3. **Substituir espaços por novas linhas**:
   Para transformar espaços em novas linhas:
   ```bash
   echo "Um dois três" | tr ' ' '\n'
   ```

4. **Compactar espaços**:
   Para substituir múltiplos espaços por um único espaço:
   ```bash
   echo "Um    dois     três" | tr -s ' '
   ```

5. **Usar complementos**:
   Para substituir todos os caracteres que não são dígitos por um espaço:
   ```bash
   echo "123abc456" | tr -c '0-9' ' '
   ```

## Tips
- Use `tr` em combinação com outros comandos, como `grep` ou `sort`, para manipular dados de forma mais poderosa.
- Sempre teste seus comandos com uma entrada de exemplo antes de aplicá-los em arquivos importantes.
- Lembre-se de que `tr` não modifica arquivos diretamente; ele sempre lê da entrada padrão e escreve na saída padrão. Para salvar as alterações, redirecione a saída para um novo arquivo.