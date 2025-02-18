# [Italiano] Debian Almquist Shell (dash) jobs uso: Gestire i processi in background

## Overview
Il comando `jobs` in dash è utilizzato per visualizzare i processi in background e in sospensione avviati dalla shell corrente. Questo comando è utile per monitorare e gestire i processi che non sono attualmente in primo piano.

## Usage
La sintassi di base del comando è la seguente:

```bash
jobs [options] [arguments]
```

## Common Options
- `-l`: Mostra il numero di processo (PID) insieme all'elenco dei lavori.
- `-n`: Mostra solo i lavori che sono cambiati di stato dall'ultima esecuzione del comando.
- `-p`: Mostra solo i PID dei lavori.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `jobs`:

1. **Visualizzare i lavori attivi**
   ```bash
   jobs
   ```

2. **Visualizzare i lavori con i loro PID**
   ```bash
   jobs -l
   ```

3. **Visualizzare solo i lavori che sono cambiati di stato**
   ```bash
   jobs -n
   ```

4. **Visualizzare solo i PID dei lavori**
   ```bash
   jobs -p
   ```

## Tips
- Usa `bg %n` per riprendere un lavoro in background, dove `n` è il numero del lavoro.
- Usa `fg %n` per portare un lavoro in primo piano.
- Ricorda che i lavori in background continuano a funzionare anche se chiudi la shell, a meno che non siano stati terminati.