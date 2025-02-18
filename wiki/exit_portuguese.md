# [Português] Debian Almquist Shell (dash) exit uso: Finaliza um script ou sessão de shell

## Overview
O comando `exit` é utilizado para encerrar um script ou uma sessão do shell. Ele finaliza a execução do shell atual e, opcionalmente, pode retornar um código de saída que indica o status da execução.

## Usage
A sintaxe básica do comando `exit` é a seguinte:

```bash
exit [código]
```

Onde `[código]` é um número que representa o código de saída desejado. Se não for especificado, o código de saída padrão é o do último comando executado.

## Common Options
O comando `exit` não possui opções específicas, mas aceita um argumento que é o código de saída:

- `código`: Um número inteiro que representa o código de saída. Por convenção, um código de saída de `0` indica sucesso, enquanto qualquer número diferente de `0` indica um erro.

## Common Examples

1. **Sair de um script com sucesso:**
   ```bash
   exit 0
   ```

2. **Sair de um script com um código de erro:**
   ```bash
   exit 1
   ```

3. **Sair de uma sessão interativa do shell:**
   ```bash
   exit
   ```

4. **Sair de um script e retornar um código de erro específico:**
   ```bash
   if [ ! -f "arquivo.txt" ]; then
       echo "Arquivo não encontrado!"
       exit 2
   fi
   ```

## Tips
- Sempre utilize um código de saída apropriado para facilitar a depuração de scripts.
- Em scripts complexos, considere usar códigos de saída diferentes para diferentes tipos de erros, assim você pode identificar rapidamente a causa do problema.
- Lembre-se de que o código de saída do último comando executado pode ser acessado através da variável especial `$?`, o que pode ser útil antes de chamar `exit`.