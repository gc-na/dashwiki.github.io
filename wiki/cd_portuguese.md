# [Português] Debian Almquist Shell (dash) cd uso: Mudar diretórios

## Overview
O comando `cd` (change directory) é utilizado no shell para mudar o diretório de trabalho atual. Isso permite que você navegue entre diferentes diretórios no sistema de arquivos.

## Usage
A sintaxe básica do comando `cd` é a seguinte:

```bash
cd [opções] [argumentos]
```

## Common Options
Embora o comando `cd` não tenha muitas opções, aqui estão algumas comuns:

- `-`: Muda para o diretório anterior.
- `..`: Muda para o diretório pai do diretório atual.
- `~`: Muda para o diretório home do usuário atual.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `cd`:

1. Mudar para um diretório específico:
   ```bash
   cd /caminho/para/o/diretorio
   ```

2. Voltar para o diretório anterior:
   ```bash
   cd -
   ```

3. Subir um nível na hierarquia de diretórios:
   ```bash
   cd ..
   ```

4. Ir para o diretório home do usuário:
   ```bash
   cd ~
   ```

5. Mudar para um diretório relativo:
   ```bash
   cd pasta/subpasta
   ```

## Tips
- Utilize `cd -` para alternar rapidamente entre dois diretórios.
- Use `cd ..` para navegar de forma eficiente para diretórios superiores.
- Para evitar erros de digitação, você pode usar o recurso de autocompletar pressionando a tecla `Tab` após digitar parte do nome do diretório.