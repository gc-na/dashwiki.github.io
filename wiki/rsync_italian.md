# [Italiano] Debian Almquist Shell (dash) rsync uso: Sincronizzare file e directory

## Overview
Il comando `rsync` è uno strumento potente per la sincronizzazione di file e directory tra diverse posizioni, sia localmente che su reti. È particolarmente utile per il backup e la copia di file in modo efficiente, poiché trasferisce solo le parti modificate dei file.

## Usage
La sintassi di base del comando `rsync` è la seguente:

```bash
rsync [opzioni] [origine] [destinazione]
```

## Common Options
Ecco alcune opzioni comuni per `rsync`:

- `-a`: Modalità archivio; copia ricorsivamente e conserva i permessi, i timestamp e i link simbolici.
- `-v`: Modalità verbosa; mostra i dettagli del trasferimento.
- `-z`: Comprimi i dati durante il trasferimento per risparmiare banda.
- `-r`: Copia ricorsivamente le directory.
- `--delete`: Elimina i file nella destinazione che non sono presenti nell'origine.

## Common Examples
Ecco alcuni esempi pratici di utilizzo di `rsync`:

1. **Sincronizzare una directory locale con un'altra directory locale:**

   ```bash
   rsync -av /percorso/origine/ /percorso/destinazione/
   ```

2. **Sincronizzare una directory locale con un server remoto:**

   ```bash
   rsync -av /percorso/origine/ utente@server:/percorso/destinazione/
   ```

3. **Sincronizzare una directory remota con una directory locale:**

   ```bash
   rsync -av utente@server:/percorso/origine/ /percorso/destinazione/
   ```

4. **Sincronizzare e comprimere i dati durante il trasferimento:**

   ```bash
   rsync -avz /percorso/origine/ utente@server:/percorso/destinazione/
   ```

5. **Sincronizzare e rimuovere i file non presenti nell'origine:**

   ```bash
   rsync -av --delete /percorso/origine/ /percorso/destinazione/
   ```

## Tips
- Assicurati di utilizzare sempre una barra finale (`/`) nella directory di origine se desideri copiare solo il contenuto della directory e non la directory stessa.
- Utilizza l'opzione `-n` (dry run) per simulare il trasferimento senza effettivamente copiare i file, utile per verificare cosa verrà trasferito.
- Considera di utilizzare `rsync` in combinazione con cron per automatizzare i backup regolari.