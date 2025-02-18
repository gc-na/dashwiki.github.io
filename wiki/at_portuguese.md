# [Português] Debian Almquist Shell (dash) at: Agendar tarefas para execução futura

## Overview
O comando `at` é utilizado para agendar a execução de comandos ou scripts em um horário específico no futuro. Ele permite que os usuários programem tarefas que serão executadas uma única vez, facilitando a automação de processos.

## Usage
A sintaxe básica do comando `at` é a seguinte:

```
at [opções] [hora]
```

## Common Options
- `-f <arquivo>`: Especifica um arquivo que contém os comandos a serem executados.
- `-m`: Envia um e-mail ao usuário após a execução do comando, mesmo que não haja saída.
- `-q <fila>`: Define a fila de execução do comando (pode ser útil para priorizar tarefas).
- `-v`: Exibe informações sobre a execução do comando agendado.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `at`:

1. **Agendar um comando para ser executado agora:**
   ```bash
   echo "echo 'Olá, mundo!'" | at now
   ```

2. **Agendar um comando para ser executado em 5 minutos:**
   ```bash
   echo "backup.sh" | at now + 5 minutes
   ```

3. **Agendar um comando para ser executado em uma data e hora específica:**
   ```bash
   echo "shutdown -h now" | at 22:00
   ```

4. **Usar um arquivo para agendar múltiplos comandos:**
   ```bash
   at -f meus_comandos.sh 10:00
   ```

5. **Agendar um comando e receber um e-mail após a execução:**
   ```bash
   echo "echo 'Tarefa concluída!'" | at -m now + 1 hour
   ```

## Tips
- Sempre verifique se o serviço `atd` está em execução no seu sistema, pois ele é necessário para que as tarefas agendadas sejam executadas.
- Utilize `atq` para listar as tarefas agendadas e `atrm <número>` para remover uma tarefa específica.
- Para evitar conflitos, agende tarefas em horários que não sobreponham outras tarefas críticas.