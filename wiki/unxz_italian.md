# [Italiano] Debian Almquist Shell (dash) unxz: Decomprimere file .xz

## Overview
Il comando `unxz` viene utilizzato per decomprimere file compressi con l'algoritmo XZ. Questo strumento è utile per ripristinare file in formato originale dopo che sono stati compressi, risparmiando spazio su disco.

## Usage
La sintassi di base del comando è la seguente:

```bash
unxz [opzioni] [argomenti]
```

## Common Options
- `-k`, `--keep`: Mantiene il file compresso originale dopo la decompressione.
- `-f`, `--force`: Sovrascrive i file esistenti senza chiedere conferma.
- `-v`, `--verbose`: Mostra informazioni dettagliate durante il processo di decompressione.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `unxz`:

1. Decomprimere un file .xz:
   ```bash
   unxz file.xz
   ```

2. Decomprimere un file .xz e mantenere il file originale:
   ```bash
   unxz -k file.xz
   ```

3. Forzare la decompressione sovrascrivendo un file esistente:
   ```bash
   unxz -f file.xz
   ```

4. Decomprimere più file .xz in una sola volta:
   ```bash
   unxz file1.xz file2.xz file3.xz
   ```

5. Decomprimere un file e visualizzare il processo:
   ```bash
   unxz -v file.xz
   ```

## Tips
- Assicurati di avere spazio sufficiente sul disco prima di decomprimere file di grandi dimensioni.
- Utilizza l'opzione `-k` se desideri mantenere il file compresso originale per future necessità.
- Controlla sempre i file decompressi per assicurarti che non ci siano stati errori durante il processo.