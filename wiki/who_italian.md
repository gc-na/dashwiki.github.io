# [Italiano] Debian Almquist Shell (dash) who: visualizza gli utenti connessi

## Overview
Il comando `who` in dash è utilizzato per visualizzare gli utenti attualmente connessi al sistema. Mostra informazioni come il nome dell'utente, il terminale utilizzato, la data e l'ora dell'accesso.

## Usage
La sintassi di base del comando è la seguente:

```
who [options] [arguments]
```

## Common Options
- `-a`: Mostra tutte le informazioni disponibili, inclusi gli utenti inattivi.
- `-b`: Mostra l'ora dell'ultimo riavvio del sistema.
- `-q`: Mostra solo i nomi degli utenti connessi e il conteggio totale.
- `--help`: Mostra un messaggio di aiuto con le opzioni disponibili.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `who`:

1. Visualizzare gli utenti attualmente connessi:
   ```bash
   who
   ```

2. Visualizzare tutte le informazioni sugli utenti, inclusi quelli inattivi:
   ```bash
   who -a
   ```

3. Mostrare l'ora dell'ultimo riavvio del sistema:
   ```bash
   who -b
   ```

4. Visualizzare solo i nomi degli utenti connessi e il conteggio totale:
   ```bash
   who -q
   ```

## Tips
- Utilizza `who -b` per controllare quando è stato riavviato il sistema, utile per la gestione della manutenzione.
- Se desideri monitorare gli accessi in tempo reale, considera di combinare `who` con il comando `watch`:
  ```bash
  watch who
  ```
- Ricorda che il comando `who` mostra solo gli utenti connessi localmente; per vedere anche gli utenti remoti, puoi utilizzare `w` o `users`.