# [Português] Debian Almquist Shell (dash) mkdir Uso: Criação de diretórios

## Overview
O comando `mkdir` é utilizado para criar novos diretórios no sistema de arquivos. É uma ferramenta fundamental para organizar arquivos e pastas de maneira hierárquica.

## Usage
A sintaxe básica do comando `mkdir` é a seguinte:

```bash
mkdir [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o comando `mkdir`:

- `-p`: Cria diretórios pai conforme necessário. Se os diretórios intermediários não existirem, eles serão criados.
- `-v`: Modo verbose, que exibe uma mensagem para cada diretório criado.
- `-m`: Define as permissões do diretório criado, utilizando a notação octal.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `mkdir`:

1. **Criar um diretório simples:**
   ```bash
   mkdir meu_diretorio
   ```

2. **Criar múltiplos diretórios ao mesmo tempo:**
   ```bash
   mkdir dir1 dir2 dir3
   ```

3. **Criar um diretório com diretórios pai:**
   ```bash
   mkdir -p /caminho/para/meu_diretorio
   ```

4. **Criar um diretório e mostrar uma mensagem:**
   ```bash
   mkdir -v novo_diretorio
   ```

5. **Criar um diretório com permissões específicas:**
   ```bash
   mkdir -m 755 meu_diretorio
   ```

## Tips
- Sempre verifique se o diretório que você está tentando criar já existe para evitar erros.
- Utilize a opção `-p` quando precisar criar uma estrutura de diretórios complexa em um único comando.
- Combine o uso de `mkdir` com outros comandos, como `cd`, para facilitar a navegação após a criação do diretório.