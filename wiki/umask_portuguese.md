# [Português] Debian Almquist Shell (dash) umask: Define permissões padrão de arquivos

## Overview
O comando `umask` é utilizado para definir as permissões padrão de arquivos e diretórios criados em um sistema Unix-like. Ele especifica quais permissões serão removidas das permissões padrão ao criar novos arquivos e diretórios.

## Usage
A sintaxe básica do comando `umask` é a seguinte:

```
umask [opções] [máscara]
```

## Common Options
- `-S`: Exibe a máscara de permissões em um formato simbólico.
- `-p`: Exibe a máscara atual de forma persistente.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `umask`:

1. **Verificar a máscara atual:**
   ```sh
   umask
   ```

2. **Definir uma nova máscara:**
   ```sh
   umask 027
   ```

3. **Exibir a máscara em formato simbólico:**
   ```sh
   umask -S
   ```

4. **Definir a máscara para permitir leitura e escrita apenas para o proprietário:**
   ```sh
   umask 077
   ```

5. **Restaurar a máscara padrão:**
   ```sh
   umask 022
   ```

## Tips
- Sempre verifique a máscara atual antes de definir uma nova para evitar permissões indesejadas.
- Use a opção `-S` para entender melhor como suas configurações de máscara afetam as permissões.
- Considere as implicações de segurança ao definir permissões mais restritivas, especialmente em ambientes multiusuário.