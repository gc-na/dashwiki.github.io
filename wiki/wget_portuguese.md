# [Português] Debian Almquist Shell (dash) wget uso: Ferramenta para download de arquivos da web

## Overview
O comando `wget` é uma ferramenta de linha de comando utilizada para baixar arquivos da web. Ele suporta diversos protocolos, como HTTP, HTTPS e FTP, e é amplamente utilizado para automatizar downloads de arquivos.

## Usage
A sintaxe básica do comando `wget` é a seguinte:

```bash
wget [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do `wget`:

- `-O <arquivo>`: Especifica o nome do arquivo de saída.
- `-c`: Continua um download interrompido.
- `-q`: Executa o comando em modo silencioso, sem exibir mensagens.
- `--limit-rate=<taxa>`: Limita a taxa de download a um valor especificado.
- `-r`: Ativa o modo recursivo, permitindo baixar diretórios inteiros.

## Common Examples
Aqui estão alguns exemplos práticos de como usar o `wget`:

1. **Baixar um único arquivo:**
   ```bash
   wget http://exemplo.com/arquivo.txt
   ```

2. **Baixar um arquivo e renomeá-lo:**
   ```bash
   wget -O novo_nome.txt http://exemplo.com/arquivo.txt
   ```

3. **Continuar um download interrompido:**
   ```bash
   wget -c http://exemplo.com/arquivo_grande.zip
   ```

4. **Baixar um diretório inteiro recursivamente:**
   ```bash
   wget -r http://exemplo.com/diretorio/
   ```

5. **Baixar um arquivo em modo silencioso:**
   ```bash
   wget -q http://exemplo.com/arquivo.txt
   ```

## Tips
- Sempre verifique a URL antes de iniciar o download para garantir que você está baixando o arquivo correto.
- Use a opção `-c` para evitar perder tempo em downloads grandes que podem ser interrompidos.
- Considere usar `--limit-rate` se você estiver em uma conexão com largura de banda limitada para não sobrecarregar a rede.
- Para downloads recursivos, tenha cuidado com sites que podem ter restrições de acesso ou que não permitem scraping.