# [Português] Debian Almquist Shell (dash) nohup uso: Executar comandos sem interrupções

## Overview
O comando `nohup` é utilizado para executar processos que continuam em execução mesmo após o usuário ter feito logout do sistema. Isso é especialmente útil para tarefas longas que você não quer que sejam interrompidas.

## Usage
A sintaxe básica do comando `nohup` é a seguinte:

```
nohup [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do `nohup`:

- `&`: Coloca o comando em segundo plano, permitindo que você continue usando o terminal.
- `-o [arquivo]`: Especifica um arquivo para redirecionar a saída padrão do comando.
- `-e [arquivo]`: Especifica um arquivo para redirecionar a saída de erro.

## Common Examples
Aqui estão alguns exemplos práticos do uso do `nohup`:

1. Executar um script em segundo plano:
   ```bash
   nohup ./meu_script.sh &
   ```

2. Executar um comando e redirecionar a saída para um arquivo:
   ```bash
   nohup ping google.com > saida_ping.txt &
   ```

3. Executar um comando e redirecionar a saída de erro:
   ```bash
   nohup ./meu_programa 2> erro.txt &
   ```

4. Executar um comando com saída padrão e de erro redirecionadas para o mesmo arquivo:
   ```bash
   nohup ./meu_programa > saida.txt 2>&1 &
   ```

## Tips
- Sempre use `&` se você quiser continuar usando o terminal enquanto o comando está em execução.
- Verifique o arquivo `nohup.out` se você não especificou um arquivo de saída, pois a saída padrão será redirecionada para lá.
- Utilize `jobs` e `fg` para gerenciar processos em segundo plano, se necessário.