# [Português] Debian Almquist Shell (dash) sed Uso: Editar texto em streams

## Overview
O comando `sed` (Stream Editor) é uma ferramenta poderosa utilizada para manipulação de texto em streams. Ele permite realizar operações como substituição, inserção e exclusão de texto em arquivos ou na entrada padrão.

## Usage
A sintaxe básica do comando `sed` é a seguinte:

```bash
sed [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do `sed`:

- `-e`: Permite adicionar múltiplas expressões de edição.
- `-i`: Edita os arquivos no local, ou seja, faz as alterações diretamente nos arquivos originais.
- `-n`: Suprime a saída padrão, permitindo que você controle o que é exibido.
- `s/padrão/substituição/`: Realiza uma substituição do padrão pelo texto especificado.

## Common Examples
Aqui estão alguns exemplos práticos do uso do `sed`:

1. **Substituir uma palavra em um arquivo:**
   ```bash
   sed 's/antigo/novo/' arquivo.txt
   ```

2. **Substituir todas as ocorrências de uma palavra:**
   ```bash
   sed 's/antigo/novo/g' arquivo.txt
   ```

3. **Editar um arquivo no local:**
   ```bash
   sed -i 's/antigo/novo/g' arquivo.txt
   ```

4. **Remover linhas que contêm uma palavra específica:**
   ```bash
   sed '/palavra/d' arquivo.txt
   ```

5. **Exibir apenas linhas que contêm uma palavra:**
   ```bash
   sed -n '/palavra/p' arquivo.txt
   ```

## Tips
- Sempre faça uma cópia de segurança dos arquivos antes de usar a opção `-i`, pois as alterações são irreversíveis.
- Utilize a opção `-n` em combinação com o comando `p` para controlar a saída e exibir apenas as linhas desejadas.
- Teste suas expressões `sed` em um terminal antes de aplicá-las em arquivos importantes para evitar erros.