# [Italiano] Debian Almquist Shell (dash) wget uso: Scaricare file da internet

## Overview
Il comando `wget` è uno strumento potente utilizzato per scaricare file da internet. Supporta vari protocolli, tra cui HTTP, HTTPS e FTP, ed è in grado di gestire download in background, riprendere download interrotti e scaricare interi siti web.

## Usage
La sintassi di base del comando `wget` è la seguente:

```bash
wget [opzioni] [argomenti]
```

## Common Options
Ecco alcune opzioni comuni per `wget`:

- `-O [file]`: Specifica il nome del file di output.
- `-c`: Riprende un download interrotto.
- `-q`: Esegue il download in modalità silenziosa, senza output sul terminale.
- `--limit-rate=[speed]`: Limita la velocità di download a una certa velocità.
- `-r`: Scarica in modo ricorsivo, utile per scaricare interi siti web.

## Common Examples
Ecco alcuni esempi pratici di utilizzo di `wget`:

1. Scaricare un file da un URL specifico:

   ```bash
   wget https://example.com/file.zip
   ```

2. Scaricare un file e salvarlo con un nome specifico:

   ```bash
   wget -O miofile.zip https://example.com/file.zip
   ```

3. Riprendere un download interrotto:

   ```bash
   wget -c https://example.com/file.zip
   ```

4. Scaricare un intero sito web in modo ricorsivo:

   ```bash
   wget -r https://example.com
   ```

5. Limitare la velocità di download:

   ```bash
   wget --limit-rate=200k https://example.com/file.zip
   ```

## Tips
- Utilizza l'opzione `-q` per ridurre il rumore nel terminale durante download lunghi.
- Se stai scaricando un sito web, considera di utilizzare l'opzione `-np` (no parent) per evitare di risalire nella gerarchia delle directory.
- Controlla sempre i permessi e le politiche di utilizzo del sito web prima di scaricare contenuti per evitare violazioni.