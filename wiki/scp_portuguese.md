# [Português] Debian Almquist Shell (dash) scp Uso: Transferir arquivos de forma segura

## Overview
O comando `scp` (Secure Copy Protocol) é utilizado para transferir arquivos e diretórios entre sistemas de forma segura, utilizando o protocolo SSH (Secure Shell). Ele permite que você copie arquivos de um computador para outro, garantindo que os dados sejam criptografados durante a transferência.

## Usage
A sintaxe básica do comando `scp` é a seguinte:

```bash
scp [opções] [origem] [destino]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o `scp`:

- `-r`: Copia diretórios recursivamente.
- `-P`: Especifica a porta do SSH (note que é um P maiúsculo).
- `-i`: Especifica um arquivo de chave privada para autenticação.
- `-v`: Ativa o modo verbose, exibindo informações detalhadas sobre a transferência.

## Common Examples
Aqui estão alguns exemplos práticos de como usar o `scp`:

1. **Copiar um arquivo do seu computador local para um servidor remoto:**
   ```bash
   scp arquivo.txt usuario@servidor:/caminho/destino/
   ```

2. **Copiar um arquivo de um servidor remoto para o seu computador local:**
   ```bash
   scp usuario@servidor:/caminho/origem/arquivo.txt /caminho/destino/
   ```

3. **Copiar um diretório inteiro do seu computador local para um servidor remoto:**
   ```bash
   scp -r meu_diretorio usuario@servidor:/caminho/destino/
   ```

4. **Copiar um arquivo usando uma porta SSH diferente:**
   ```bash
   scp -P 2222 arquivo.txt usuario@servidor:/caminho/destino/
   ```

## Tips
- Sempre verifique as permissões de arquivos e diretórios no servidor remoto para garantir que você tenha acesso de escrita.
- Utilize a opção `-v` para depuração se encontrar problemas durante a transferência.
- Considere usar chaves SSH para autenticação em vez de senhas, pois isso aumenta a segurança e facilita o processo de login.