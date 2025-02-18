# [Italiano] Debian Almquist Shell (dash) mkdir utilizzo: Crea directory

## Overview
Il comando `mkdir` è utilizzato per creare nuove directory nel file system. È uno strumento fondamentale per l'organizzazione dei file e delle cartelle.

## Usage
La sintassi di base del comando è la seguente:

```bash
mkdir [opzioni] [argomenti]
```

## Common Options
- `-p`: Crea directory genitore se non esistono già.
- `-m`: Imposta i permessi della directory utilizzando la modalità specificata.
- `-v`: Mostra un messaggio per ogni directory creata.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `mkdir`:

1. Creare una singola directory:
   ```bash
   mkdir nuova_cartella
   ```

2. Creare più directory contemporaneamente:
   ```bash
   mkdir cartella1 cartella2 cartella3
   ```

3. Creare una directory con directory genitore:
   ```bash
   mkdir -p /home/utente/progetti/nuovo_progetto
   ```

4. Creare una directory e impostare i permessi:
   ```bash
   mkdir -m 755 cartella_privata
   ```

5. Creare una directory e visualizzare un messaggio:
   ```bash
   mkdir -v cartella_visibile
   ```

## Tips
- Utilizza l'opzione `-p` quando hai bisogno di creare una struttura di directory complessa senza preoccuparti se le directory genitore esistono già.
- Controlla i permessi delle directory create con `ls -l` per assicurarti che siano impostati correttamente.
- Ricorda di utilizzare nomi di directory descrittivi per facilitare l'organizzazione dei tuoi file.