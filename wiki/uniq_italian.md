# [Italiano] Debian Almquist Shell (dash) uniq Uso equivalente: Rimuovere le righe duplicate

## Overview
Il comando `uniq` viene utilizzato per filtrare le righe duplicate da un file o da un input standard. Esso restituisce solo le righe uniche, rendendo utile la pulizia dei dati e l'analisi dei file di testo.

## Usage
La sintassi di base del comando `uniq` è la seguente:

```bash
uniq [options] [arguments]
```

## Common Options
- `-c`: Conta il numero di occorrenze di ogni riga e visualizza il conteggio accanto alla riga.
- `-d`: Mostra solo le righe duplicate.
- `-u`: Mostra solo le righe uniche, escludendo quelle duplicate.
- `-i`: Ignora la differenza tra maiuscole e minuscole durante il confronto delle righe.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `uniq`:

1. Rimuovere righe duplicate da un file:
   ```bash
   uniq file.txt
   ```

2. Contare le occorrenze di ogni riga:
   ```bash
   uniq -c file.txt
   ```

3. Visualizzare solo le righe duplicate:
   ```bash
   uniq -d file.txt
   ```

4. Visualizzare solo le righe uniche:
   ```bash
   uniq -u file.txt
   ```

5. Ignorare la differenza tra maiuscole e minuscole:
   ```bash
   uniq -i file.txt
   ```

## Tips
- Assicurati che il file di input sia ordinato prima di utilizzare `uniq`, poiché il comando funziona meglio su dati già ordinati.
- Puoi combinare `uniq` con altri comandi come `sort` per ottenere risultati più utili:
  ```bash
  sort file.txt | uniq
  ```
- Utilizza l'opzione `-c` per avere un'idea di quante volte ogni riga appare nel file, utile per analisi statistiche.