# [Português] Debian Almquist Shell (dash) ftp Uso: Transferência de arquivos

## Overview
O comando `ftp` é utilizado para transferir arquivos entre um cliente e um servidor utilizando o protocolo File Transfer Protocol (FTP). Ele permite que os usuários se conectem a servidores FTP, façam upload e download de arquivos, e gerenciem diretórios remotos.

## Usage
A sintaxe básica do comando `ftp` é a seguinte:

```bash
ftp [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do comando `ftp`:

- `-i`: Desativa o modo interativo, permitindo transferências de arquivos sem confirmação.
- `-v`: Ativa o modo verbose, exibindo informações detalhadas sobre a transferência.
- `-n`: Impede a conexão automática ao servidor, permitindo que o usuário se conecte manualmente.
- `-p`: Utiliza uma porta passiva para a conexão, útil em firewalls.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `ftp`:

1. Conectar a um servidor FTP:
   ```bash
   ftp ftp.exemplo.com
   ```

2. Fazer upload de um arquivo para o servidor:
   ```bash
   put arquivo.txt
   ```

3. Fazer download de um arquivo do servidor:
   ```bash
   get arquivo.txt
   ```

4. Listar arquivos no diretório remoto:
   ```bash
   ls
   ```

5. Mudar para um diretório específico no servidor:
   ```bash
   cd /diretorio/exemplo
   ```

## Tips
- Sempre verifique se você tem permissões adequadas para acessar e transferir arquivos no servidor FTP.
- Utilize o modo interativo (`-i`) para transferências em massa, evitando confirmações desnecessárias.
- Considere usar um cliente FTP gráfico se você preferir uma interface mais amigável para transferências de arquivos.