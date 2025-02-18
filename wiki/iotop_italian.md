# [Italiano] Debian Almquist Shell (dash) iotop: Monitora l'uso del disco in tempo reale

## Overview
Il comando `iotop` è uno strumento utile per monitorare l'uso del disco in tempo reale da parte dei processi in esecuzione su un sistema. Consente di visualizzare quali processi stanno generando più attività di I/O, fornendo informazioni preziose per l'ottimizzazione delle prestazioni del sistema.

## Usage
La sintassi di base del comando è la seguente:

```bash
iotop [options] [arguments]
```

## Common Options
- `-o`, `--only`: Mostra solo i processi che stanno attualmente effettuando operazioni di I/O.
- `-b`, `--batch`: Esegue `iotop` in modalità batch, utile per l'output su file o per l'analisi automatizzata.
- `-d`, `--delay`: Imposta il ritardo in secondi tra gli aggiornamenti dell'interfaccia (default è 1 secondo).
- `-p`, `--pid`: Monitora solo il processo con l'ID specificato.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `iotop`:

1. **Visualizzare l'uso del disco in tempo reale:**
   ```bash
   iotop
   ```

2. **Mostrare solo i processi attivi:**
   ```bash
   iotop -o
   ```

3. **Eseguire `iotop` in modalità batch per 10 secondi:**
   ```bash
   iotop -b -d 10
   ```

4. **Monitorare un processo specifico con ID 1234:**
   ```bash
   iotop -p 1234
   ```

## Tips
- Utilizza l'opzione `-o` per filtrare i processi che stanno effettivamente utilizzando il disco, rendendo l'output più rilevante.
- Se hai bisogno di registrare l'output per analisi future, considera di utilizzare la modalità batch con un reindirizzamento dell'output.
- Ricorda che `iotop` richiede privilegi di root per visualizzare le informazioni sui processi di altri utenti, quindi potresti dover eseguire il comando con `sudo`.