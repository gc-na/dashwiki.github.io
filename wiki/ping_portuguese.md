# [Português] Debian Almquist Shell (dash) ping uso: Verificar conectividade de rede

## Overview
O comando `ping` é utilizado para verificar a conectividade de rede entre o seu computador e outro dispositivo na rede, enviando pacotes de dados e aguardando uma resposta. É uma ferramenta essencial para diagnosticar problemas de rede.

## Usage
A sintaxe básica do comando `ping` é a seguinte:

```bash
ping [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o comando `ping`:

- `-c [n]`: Envia apenas `n` pacotes de dados.
- `-i [s]`: Define o intervalo em segundos entre o envio de pacotes.
- `-t [n]`: Define o tempo de vida (TTL) dos pacotes.
- `-s [n]`: Especifica o tamanho do pacote a ser enviado.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `ping`:

1. **Pingar um endereço IP ou domínio:**
   ```bash
   ping google.com
   ```

2. **Enviar apenas 4 pacotes:**
   ```bash
   ping -c 4 google.com
   ```

3. **Definir um intervalo de 2 segundos entre os pacotes:**
   ```bash
   ping -i 2 google.com
   ```

4. **Alterar o tamanho do pacote para 128 bytes:**
   ```bash
   ping -s 128 google.com
   ```

## Tips
- Utilize a opção `-c` para limitar o número de pacotes enviados, evitando sobrecarregar a rede.
- Verifique a conectividade com diferentes servidores para diagnosticar problemas específicos.
- Se você não receber respostas, verifique se o dispositivo de destino está ativo e se não há problemas de firewall.