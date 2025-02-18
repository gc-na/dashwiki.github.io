# [Português] Debian Almquist Shell (dash) netstat Uso: Exibir conexões de rede

## Overview
O comando `netstat` é uma ferramenta de linha de comando que exibe informações sobre conexões de rede, tabelas de roteamento e estatísticas de interface. É útil para monitorar o tráfego de rede e diagnosticar problemas de conectividade.

## Usage
A sintaxe básica do comando `netstat` é a seguinte:

```bash
netstat [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do `netstat`:

- `-a`: Exibe todas as conexões e escuta portas.
- `-t`: Mostra apenas conexões TCP.
- `-u`: Mostra apenas conexões UDP.
- `-n`: Exibe endereços e números de porta em formato numérico.
- `-l`: Exibe apenas as portas que estão escutando.
- `-p`: Mostra o PID e o nome do programa que está usando a conexão.

## Common Examples
Aqui estão alguns exemplos práticos do uso do `netstat`:

1. **Exibir todas as conexões e portas em escuta:**
   ```bash
   netstat -a
   ```

2. **Mostrar apenas conexões TCP:**
   ```bash
   netstat -t
   ```

3. **Mostrar apenas conexões UDP:**
   ```bash
   netstat -u
   ```

4. **Exibir conexões em formato numérico:**
   ```bash
   netstat -n
   ```

5. **Listar portas que estão escutando:**
   ```bash
   netstat -l
   ```

6. **Mostrar conexões com o PID e nome do programa:**
   ```bash
   netstat -p
   ```

## Tips
- Utilize a opção `-n` para acelerar a exibição de conexões, evitando a resolução de nomes de host.
- Combine opções para obter informações mais detalhadas, como `netstat -tuln` para ver conexões TCP e UDP que estão escutando em formato numérico.
- Verifique regularmente as conexões de rede para identificar atividades suspeitas ou problemas de desempenho.