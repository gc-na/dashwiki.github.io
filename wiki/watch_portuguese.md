# [Português] Debian Almquist Shell (dash) watch uso: Monitore a saída de comandos

## Overview
O comando `watch` permite que você execute um comando periodicamente e visualize a saída em tempo real. É útil para monitorar mudanças em arquivos, processos ou qualquer outra saída que você deseje observar ao longo do tempo.

## Usage
A sintaxe básica do comando `watch` é a seguinte:

```bash
watch [opções] [comando]
```

## Common Options
Aqui estão algumas opções comuns do comando `watch`:

- `-n, --interval <segundos>`: Define o intervalo de tempo em segundos entre as execuções do comando. O padrão é 2 segundos.
- `-d, --differences`: Destaca as diferenças entre as saídas sucessivas.
- `-t, --no-title`: Remove o título da janela do `watch`, mostrando apenas a saída do comando.

## Common Examples

1. **Monitorar o uso de memória:**
   ```bash
   watch -n 5 free -h
   ```
   Este comando executa `free -h` a cada 5 segundos, permitindo que você veja a utilização de memória em tempo real.

2. **Verificar o espaço em disco:**
   ```bash
   watch df -h
   ```
   Aqui, o comando `df -h` é executado a cada 2 segundos (padrão), mostrando o uso do espaço em disco.

3. **Monitorar um diretório para alterações:**
   ```bash
   watch -d ls -l /caminho/para/diretorio
   ```
   Este comando lista o conteúdo do diretório especificado e destaca as mudanças entre as execuções.

4. **Verificar processos em execução:**
   ```bash
   watch -n 1 ps aux
   ```
   Este comando executa `ps aux` a cada segundo, permitindo que você veja a lista de processos em execução.

## Tips
- Utilize a opção `-d` para facilitar a visualização de alterações, especialmente quando você está monitorando saídas que mudam frequentemente.
- Ajuste o intervalo com a opção `-n` para evitar sobrecarga no sistema, especialmente se o comando que você está monitorando é intensivo em recursos.
- Combine `watch` com outros comandos para criar monitoramentos personalizados, como `watch -n 10 grep "erro" /var/log/syslog` para verificar erros em logs a cada 10 segundos.