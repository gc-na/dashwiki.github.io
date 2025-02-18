# [Português] Debian Almquist Shell (dash) cp Uso: Copiar arquivos e diretórios

## Overview
O comando `cp` é utilizado para copiar arquivos e diretórios no sistema de arquivos. Ele permite que você crie cópias de arquivos existentes ou mova diretórios inteiros para novos locais.

## Usage
A sintaxe básica do comando `cp` é a seguinte:

```bash
cp [opções] [origem] [destino]
```

## Common Options
Aqui estão algumas opções comuns do comando `cp`:

- `-r`: Copia diretórios de forma recursiva.
- `-i`: Pergunta antes de sobrescrever arquivos existentes.
- `-u`: Copia apenas arquivos que são mais novos que os arquivos de destino ou que não existem no destino.
- `-v`: Exibe os arquivos sendo copiados, útil para monitorar o progresso.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `cp`:

1. **Copiar um arquivo para outro local:**
   ```bash
   cp arquivo.txt /caminho/para/destino/
   ```

2. **Copiar um diretório e seu conteúdo:**
   ```bash
   cp -r /caminho/para/diretorio/ /caminho/para/destino/
   ```

3. **Copiar um arquivo e perguntar antes de sobrescrever:**
   ```bash
   cp -i arquivo.txt /caminho/para/destino/
   ```

4. **Copiar apenas arquivos mais novos:**
   ```bash
   cp -u arquivo.txt /caminho/para/destino/
   ```

5. **Copiar um arquivo e mostrar o progresso:**
   ```bash
   cp -v arquivo.txt /caminho/para/destino/
   ```

## Tips
- Sempre verifique o caminho de destino para evitar sobrescrever arquivos importantes.
- Use a opção `-i` se você não tiver certeza se deseja sobrescrever arquivos existentes.
- Para cópias de segurança, considere usar `cp -r` para garantir que todos os arquivos e subdiretórios sejam copiados.
- Combine opções para personalizar o comportamento do comando, como `cp -ruv` para copiar apenas arquivos novos e mostrar o progresso.