# [Linux] Debian Almquist Shell (dash) traceroute6 Uso: Rastrear rotas de pacotes IPv6

## Overview
O comando `traceroute6` é utilizado para rastrear a rota que os pacotes IPv6 seguem até um destino específico. Ele ajuda a diagnosticar problemas de rede, mostrando cada salto que o pacote faz até chegar ao seu destino final.

## Usage
A sintaxe básica do comando `traceroute6` é a seguinte:

```bash
traceroute6 [opções] [destino]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o `traceroute6`:

- `-m <máx_hops>`: Define o número máximo de saltos (hops) que o comando irá seguir.
- `-p <porta>`: Especifica a porta de destino a ser usada.
- `-w <tempo>`: Define o tempo de espera (em segundos) para cada resposta.
- `-q <número>`: Especifica o número de consultas a serem enviadas por salto.

## Common Examples
Aqui estão alguns exemplos práticos de como usar o `traceroute6`:

1. Rastrear a rota para um endereço IPv6 específico:

    ```bash
    traceroute6 2001:db8::1
    ```

2. Definir um número máximo de saltos para 15:

    ```bash
    traceroute6 -m 15 2001:db8::1
    ```

3. Especificar uma porta de destino:

    ```bash
    traceroute6 -p 80 2001:db8::1
    ```

4. Aumentar o tempo de espera para 5 segundos:

    ```bash
    traceroute6 -w 5 2001:db8::1
    ```

5. Enviar 3 consultas por salto:

    ```bash
    traceroute6 -q 3 2001:db8::1
    ```

## Tips
- Sempre verifique se o seu sistema está configurado para suportar IPv6 antes de usar o `traceroute6`.
- Utilize a opção `-m` para limitar o número de saltos, especialmente em redes grandes, para evitar longas esperas.
- Combine opções para obter resultados mais precisos, como ajustar o tempo de espera e o número de consultas.
- Use `traceroute6` em conjunto com outros comandos de diagnóstico de rede, como `ping`, para uma análise mais completa da conectividade.