# [Português] Debian Almquist Shell (dash) dig <Uso equivalente em português>: consulta de DNS

## Overview
O comando `dig` (Domain Information Groper) é uma ferramenta utilizada para consultar informações sobre domínios e registros DNS. Ele permite que os usuários realizem consultas DNS detalhadas e obtenham respostas sobre endereços IP, registros MX, entre outros.

## Usage
A sintaxe básica do comando `dig` é a seguinte:

```bash
dig [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do `dig`:

- `@servidor`: Especifica um servidor DNS para realizar a consulta.
- `-t tipo`: Define o tipo de registro DNS a ser consultado (por exemplo, A, AAAA, MX).
- `+short`: Exibe uma saída mais concisa, mostrando apenas a resposta.
- `+trace`: Segue a cadeia de servidores DNS até encontrar a resposta.

## Common Examples
Aqui estão alguns exemplos práticos do uso do `dig`:

1. Consultar o endereço IP de um domínio:
   ```bash
   dig exemplo.com
   ```

2. Consultar registros MX de um domínio:
   ```bash
   dig -t MX exemplo.com
   ```

3. Consultar um servidor DNS específico:
   ```bash
   dig @8.8.8.8 exemplo.com
   ```

4. Obter uma resposta curta para um registro A:
   ```bash
   dig +short exemplo.com
   ```

5. Seguir a cadeia de servidores DNS:
   ```bash
   dig +trace exemplo.com
   ```

## Tips
- Utilize a opção `+short` para obter respostas mais rápidas e diretas, especialmente quando você só precisa do resultado final.
- Para resolver problemas de DNS, a opção `+trace` pode ser muito útil, pois mostra cada passo da resolução.
- Experimente diferentes tipos de registros (como AAAA para IPv6 ou TXT para informações adicionais) para obter uma visão mais completa sobre o domínio que você está consultando.