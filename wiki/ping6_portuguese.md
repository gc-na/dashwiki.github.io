# [Português] Debian Almquist Shell (dash) ping6 Uso: Verificar conectividade de rede IPv6

## Overview
O comando `ping6` é utilizado para verificar a conectividade de rede em endereços IPv6. Ele envia pacotes de eco ICMP para um host específico e aguarda uma resposta, permitindo que os usuários determinem se o host está acessível na rede.

## Usage
A sintaxe básica do comando `ping6` é a seguinte:

```bash
ping6 [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o comando `ping6`:

- `-c <n>`: Envia apenas `<n>` pacotes e depois para.
- `-i <s>`: Define o intervalo em segundos entre o envio de pacotes.
- `-w <s>`: Define o tempo máximo em segundos para esperar por respostas.
- `-s <tamanho>`: Define o tamanho do pacote a ser enviado.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `ping6`:

1. **Pingar um endereço IPv6 específico**:
   ```bash
   ping6 2001:db8::1
   ```

2. **Enviar apenas 5 pacotes**:
   ```bash
   ping6 -c 5 2001:db8::1
   ```

3. **Definir um intervalo de 2 segundos entre os pacotes**:
   ```bash
   ping6 -i 2 2001:db8::1
   ```

4. **Definir um tamanho de pacote de 1280 bytes**:
   ```bash
   ping6 -s 1280 2001:db8::1
   ```

5. **Definir um tempo máximo de espera de 10 segundos**:
   ```bash
   ping6 -w 10 2001:db8::1
   ```

## Tips
- Utilize a opção `-c` para evitar enviar pacotes indefinidamente, especialmente em redes onde você não tem controle.
- Verifique se o firewall do host de destino permite pacotes ICMPv6, pois isso pode afetar os resultados do `ping6`.
- Combine opções para personalizar seus testes de conectividade, como ajustar o tamanho do pacote e o intervalo de envio.