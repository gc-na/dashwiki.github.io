# [Italiano] Debian Almquist Shell (dash) du: misura l'uso dello spazio su disco

## Overview
Il comando `du` (disk usage) è utilizzato per stimare e riportare l'uso dello spazio su disco delle directory e dei file nel sistema. È uno strumento utile per monitorare quanto spazio occupano i file e le cartelle, aiutando a gestire le risorse di archiviazione.

## Usage
La sintassi di base del comando `du` è la seguente:

```bash
du [options] [arguments]
```

## Common Options
Ecco alcune opzioni comuni per il comando `du`:

- `-h`: Mostra le dimensioni in un formato leggibile dall'uomo (ad esempio, KB, MB).
- `-s`: Riporta solo il totale per ogni argomento, senza elencare le dimensioni delle sottodirectory.
- `-a`: Include i file oltre alle directory nel report.
- `-c`: Fornisce un totale cumulativo alla fine dell'output.
- `--max-depth=N`: Limita la profondità di visualizzazione delle directory a N livelli.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `du`:

1. **Visualizzare l'uso dello spazio su disco di una directory:**
   ```bash
   du /percorso/directory
   ```

2. **Visualizzare l'uso dello spazio in un formato leggibile:**
   ```bash
   du -h /percorso/directory
   ```

3. **Riportare solo il totale per una directory:**
   ```bash
   du -sh /percorso/directory
   ```

4. **Includere file e directory e mostrare in formato leggibile:**
   ```bash
   du -ah /percorso/directory
   ```

5. **Limitare la profondità di visualizzazione a 1 livello:**
   ```bash
   du --max-depth=1 /percorso/directory
   ```

6. **Ottenere un totale cumulativo dell'uso dello spazio:**
   ```bash
   du -ch /percorso/directory/*
   ```

## Tips
- Utilizza l'opzione `-h` per rendere più comprensibili le dimensioni, specialmente quando lavori con directory di grandi dimensioni.
- Combinare `-s` con `-h` è utile per ottenere un riepilogo rapido dell'uso dello spazio.
- Se stai cercando di liberare spazio, puoi utilizzare `du` per identificare le directory che occupano più spazio e decidere se eliminarle o spostarle.