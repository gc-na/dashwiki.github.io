# [Italiano] Debian Almquist Shell (dash) cp Uso: Copia file e directory

## Overview
Il comando `cp` è utilizzato per copiare file e directory in un sistema operativo Unix-like. Permette di duplicare contenuti da una posizione a un'altra, mantenendo la struttura dei dati.

## Usage
La sintassi di base del comando `cp` è la seguente:

```bash
cp [opzioni] [origine] [destinazione]
```

## Common Options
- `-r`: Copia ricorsivamente directory e il loro contenuto.
- `-i`: Chiede conferma prima di sovrascrivere file esistenti.
- `-u`: Copia solo i file che sono più recenti rispetto ai file di destinazione o se il file di destinazione non esiste.
- `-v`: Mostra i dettagli delle operazioni di copia eseguite.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `cp`:

1. Copiare un file in un'altra directory:
   ```bash
   cp documento.txt /home/utente/documenti/
   ```

2. Copiare una directory e il suo contenuto:
   ```bash
   cp -r /home/utente/cartella_origine /home/utente/cartella_destinazione
   ```

3. Copiare un file e chiedere conferma prima di sovrascrivere:
   ```bash
   cp -i documento.txt /home/utente/documenti/
   ```

4. Copiare solo file più recenti:
   ```bash
   cp -u documento.txt /home/utente/documenti/
   ```

5. Copiare un file e visualizzare i dettagli dell'operazione:
   ```bash
   cp -v documento.txt /home/utente/documenti/
   ```

## Tips
- Utilizza l'opzione `-i` per evitare di sovrascrivere accidentalmente file importanti.
- Quando copi directory, non dimenticare di usare l'opzione `-r` per copiare ricorsivamente.
- Controlla sempre il percorso di destinazione per assicurarti di non copiare file nella posizione sbagliata.