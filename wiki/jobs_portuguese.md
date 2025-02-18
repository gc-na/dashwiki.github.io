# [Português] Debian Almquist Shell (dash) jobs uso equivalente: gerenciar processos em segundo plano

## Overview
O comando `jobs` no Debian Almquist Shell (dash) é utilizado para listar os processos que estão sendo executados em segundo plano na sessão atual do shell. Ele permite que os usuários visualizem o estado dos trabalhos em execução, suspensos ou finalizados.

## Usage
A sintaxe básica do comando é a seguinte:

```bash
jobs [opções]
```

## Common Options
- `-l`: Exibe o PID (identificador do processo) de cada trabalho listado.
- `-n`: Mostra apenas os trabalhos que mudaram de estado desde a última execução do comando.
- `-p`: Exibe apenas os PIDs dos trabalhos.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `jobs`:

1. **Listar todos os trabalhos em segundo plano**:
   ```bash
   jobs
   ```

2. **Listar trabalhos com PIDs**:
   ```bash
   jobs -l
   ```

3. **Listar apenas trabalhos que mudaram de estado**:
   ```bash
   jobs -n
   ```

4. **Listar apenas os PIDs dos trabalhos**:
   ```bash
   jobs -p
   ```

## Tips
- Utilize o comando `bg` para retomar um trabalho suspenso em segundo plano após visualizá-lo com `jobs`.
- Para trazer um trabalho para o primeiro plano, use o comando `fg` seguido do número do trabalho.
- Mantenha um olho nos trabalhos em segundo plano para evitar que processos importantes sejam encerrados inadvertidamente.