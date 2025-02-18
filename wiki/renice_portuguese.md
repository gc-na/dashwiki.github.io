# [Português] Debian Almquist Shell (dash) renice: Ajustar a prioridade de processos

## Overview
O comando `renice` é utilizado para alterar a prioridade de execução de processos em sistemas Unix-like. A prioridade de um processo determina a quantidade de tempo de CPU que ele pode utilizar em relação a outros processos. Um valor de prioridade mais baixo significa maior prioridade.

## Usage
A sintaxe básica do comando `renice` é a seguinte:

```
renice [opções] [argumentos]
```

## Common Options
- `-n, --priority <valor>`: Define o novo valor de prioridade. O valor pode ser um número entre -20 (máxima prioridade) e 19 (mínima prioridade).
- `-p, --pid <pid>`: Especifica o ID do processo (PID) que terá sua prioridade alterada.
- `-g, --pgrp <gid>`: Altera a prioridade de todos os processos em um grupo de processos especificado pelo ID do grupo.
- `-u, --user <usuário>`: Altera a prioridade de todos os processos pertencentes ao usuário especificado.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `renice`:

1. **Alterar a prioridade de um processo específico:**
   ```bash
   renice -n 10 -p 1234
   ```
   Este comando altera a prioridade do processo com PID 1234 para 10.

2. **Alterar a prioridade de todos os processos de um usuário:**
   ```bash
   renice -n 5 -u usuario
   ```
   Este comando ajusta a prioridade de todos os processos pertencentes ao usuário "usuario" para 5.

3. **Alterar a prioridade de um grupo de processos:**
   ```bash
   renice -n -5 -g 5678
   ```
   Este comando define a prioridade de todos os processos no grupo com GID 5678 para -5.

4. **Verificar a prioridade atual de um processo:**
   ```bash
   ps -o pid,ni,cmd -p 1234
   ```
   Embora não seja um comando `renice`, este comando `ps` pode ser usado para verificar a prioridade atual (nice value) do processo com PID 1234.

## Tips
- Use `renice` com cuidado, pois aumentar a prioridade de um processo pode afetar o desempenho geral do sistema.
- Para verificar a prioridade de processos em execução, utilize o comando `ps` antes de aplicar `renice`.
- É necessário ter permissões adequadas (geralmente, ser o proprietário do processo ou ter privilégios de superusuário) para alterar a prioridade de processos que não pertencem ao seu usuário.