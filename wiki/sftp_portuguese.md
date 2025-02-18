# [Português] Debian Almquist Shell (dash) sftp Uso: Transferir arquivos de forma segura

## Overview
O comando `sftp` (Secure File Transfer Protocol) é utilizado para transferir arquivos de forma segura entre um cliente e um servidor. Ele funciona sobre o protocolo SSH, garantindo que os dados sejam criptografados durante a transferência.

## Usage
A sintaxe básica do comando `sftp` é a seguinte:

```bash
sftp [opções] [usuário@]host
```

## Common Options
Aqui estão algumas opções comuns do `sftp`:

- `-P <porta>`: Especifica a porta a ser utilizada para a conexão.
- `-o <opção>`: Permite passar opções adicionais para a conexão SSH.
- `-v`: Ativa o modo verbose, exibindo informações detalhadas sobre a conexão.

## Common Examples
Aqui estão alguns exemplos práticos do uso do `sftp`:

1. Conectar a um servidor SFTP:
   ```bash
   sftp usuario@exemplo.com
   ```

2. Transferir um arquivo do cliente para o servidor:
   ```bash
   put arquivo.txt
   ```

3. Transferir um arquivo do servidor para o cliente:
   ```bash
   get arquivo.txt
   ```

4. Listar arquivos no diretório remoto:
   ```bash
   ls
   ```

5. Mudar o diretório remoto:
   ```bash
   cd /caminho/do/diretorio
   ```

## Tips
- Sempre verifique a integridade dos arquivos transferidos, utilizando comandos como `md5sum` ou `sha256sum`.
- Utilize o modo verbose (`-v`) para depurar problemas de conexão.
- Considere usar chaves SSH para autenticação, pois isso pode simplificar o processo de login e aumentar a segurança.