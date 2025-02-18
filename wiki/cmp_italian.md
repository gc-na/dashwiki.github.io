# [Italiano] Debian Almquist Shell (dash) cmp Uso: confrontare file byte per byte

## Overview
Il comando `cmp` confronta due file byte per byte e riporta la posizione della prima differenza trovata. Se i file sono identici, non produce output. È utile per verificare l'integrità dei file o per confrontare versioni diverse di un file.

## Usage
La sintassi di base del comando è la seguente:

```bash
cmp [opzioni] [file1] [file2]
```

## Common Options
- `-l`: Mostra le differenze in formato numerico, elencando i byte diversi.
- `-s`: Non produce output, ma restituisce un codice di uscita che indica se i file sono identici o meno.
- `-i`: Specifica un numero di byte da ignorare all'inizio di ciascun file.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `cmp`:

1. Confrontare due file e visualizzare la prima differenza:
   ```bash
   cmp file1.txt file2.txt
   ```

2. Usare l'opzione `-l` per visualizzare le differenze in formato numerico:
   ```bash
   cmp -l file1.txt file2.txt
   ```

3. Verificare se due file sono identici senza output:
   ```bash
   cmp -s file1.txt file2.txt
   ```

4. Ignorare i primi 10 byte durante il confronto:
   ```bash
   cmp -i 10 file1.txt file2.txt
   ```

## Tips
- Utilizza l'opzione `-s` per script automatizzati, in modo da gestire il codice di uscita senza generare output superfluo.
- Quando confronti file di grandi dimensioni, considera l'uso dell'opzione `-l` per ottenere un elenco dettagliato delle differenze.
- Ricorda che `cmp` è case-sensitive, quindi "File.txt" e "file.txt" saranno considerati diversi.