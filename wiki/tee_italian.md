# [Italiano] Debian Almquist Shell (dash) tee uso: Scrivere in più file contemporaneamente

## Overview
Il comando `tee` è utilizzato per leggere dall'input standard e scrivere sia nell'output standard che in uno o più file. Questo è utile quando si desidera visualizzare l'output di un comando e, allo stesso tempo, salvarlo in un file.

## Usage
La sintassi di base del comando `tee` è la seguente:

```bash
tee [opzioni] [argomenti]
```

## Common Options
Ecco alcune opzioni comuni per il comando `tee`:

- `-a`, `--append`: Aggiunge l'output ai file esistenti invece di sovrascriverli.
- `-i`, `--ignore-interrupts`: Ignora i segnali di interruzione.
- `--help`: Mostra un messaggio di aiuto e termina.
- `--version`: Mostra la versione del comando `tee`.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `tee`:

1. **Scrivere l'output di un comando in un file:**

   ```bash
   echo "Ciao, Mondo!" | tee output.txt
   ```

   Questo comando scrive "Ciao, Mondo!" sia sullo schermo che nel file `output.txt`.

2. **Aggiungere l'output a un file esistente:**

   ```bash
   echo "Buongiorno!" | tee -a output.txt
   ```

   Qui, "Buongiorno!" viene aggiunto alla fine del file `output.txt` senza sovrascrivere il contenuto esistente.

3. **Scrivere l'output di più comandi in file diversi:**

   ```bash
   { echo "Prima linea"; echo "Seconda linea"; } | tee file1.txt file2.txt
   ```

   Questo comando scrive "Prima linea" e "Seconda linea" sia in `file1.txt` che in `file2.txt`.

4. **Utilizzare tee con un comando di pipeline:**

   ```bash
   ps aux | tee processi.txt | grep bash
   ```

   Qui, l'output del comando `ps aux` viene scritto nel file `processi.txt` e solo le righe contenenti "bash" vengono visualizzate sullo schermo.

## Tips
- Utilizza l'opzione `-a` per evitare di sovrascrivere file esistenti quando è necessario mantenere i dati.
- Combinare `tee` con altri comandi nella pipeline può essere molto utile per il debug e l'analisi.
- Ricorda che `tee` può scrivere in più file contemporaneamente, il che è utile per il salvataggio di log o output in più formati.