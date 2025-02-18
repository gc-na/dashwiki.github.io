# [Português] Debian Almquist Shell (dash) nslookup Uso: consulta de informações de DNS

## Overview
O comando `nslookup` é utilizado para consultar informações de servidores de nomes de domínio (DNS). Ele permite que os usuários obtenham detalhes sobre endereços IP, nomes de domínio e outros registros DNS.

## Usage
A sintaxe básica do comando `nslookup` é a seguinte:

```bash
nslookup [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do `nslookup`:

- `-type=tipo`: Especifica o tipo de registro DNS a ser consultado (por exemplo, A, AAAA, MX).
- `-timeout=segundos`: Define o tempo limite para a consulta.
- `-retry=número`: Define o número de tentativas em caso de falha na consulta.
- `-debug`: Ativa a saída de depuração para informações detalhadas sobre a consulta.

## Common Examples
Aqui estão alguns exemplos práticos do uso do `nslookup`:

1. Consultar o endereço IP de um domínio:
   ```bash
   nslookup exemplo.com
   ```

2. Consultar registros MX (Mail Exchange) de um domínio:
   ```bash
   nslookup -type=MX exemplo.com
   ```

3. Consultar um registro específico (como AAAA para IPv6):
   ```bash
   nslookup -type=AAAA exemplo.com
   ```

4. Usar um servidor DNS específico para a consulta:
   ```bash
   nslookup exemplo.com 8.8.8.8
   ```

## Tips
- Sempre verifique se você está usando o servidor DNS correto, especialmente em redes corporativas.
- Utilize a opção `-debug` para solucionar problemas de consultas que não retornam os resultados esperados.
- Experimente diferentes tipos de registros para obter uma visão mais completa do DNS de um domínio.