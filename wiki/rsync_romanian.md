# [România] Debian Almquist Shell (dash) rsync utilizare: Sincronizează fișiere și directoare

## Overview
Comanda `rsync` este un instrument puternic pentru sincronizarea fișierelor și directoarelor între două locații, fie pe aceeași mașină, fie pe mașini diferite. Aceasta este eficientă, deoarece transferă doar fișierele care s-au schimbat, economisind astfel lățimea de bandă și timpul de transfer.

## Usage
Sintaxa de bază a comenzii `rsync` este următoarea:

```bash
rsync [opțiuni] [sursă] [destinație]
```

## Common Options
Iată câteva opțiuni comune pentru `rsync`:

- `-a`: Activează modul arhivă, care păstrează permisiunile, timpii de modificare și simbolurile de legătură.
- `-v`: Activează modul detaliat, care oferă informații despre fișierele transferate.
- `-z`: Comprimă datele în timpul transferului pentru a economisi lățimea de bandă.
- `-r`: Recursiv, pentru a copia directoare și subdirectoare.
- `--delete`: Șterge fișierele din destinație care nu mai există în sursă.

## Common Examples
Iată câteva exemple practice ale utilizării comenzii `rsync`:

1. **Sincronizarea unui director local:**
   ```bash
   rsync -av /cale/catre/sursa/ /cale/catre/destinatie/
   ```

2. **Sincronizarea cu un server remote:**
   ```bash
   rsync -avz /cale/catre/sursa/ utilizator@server:/cale/catre/destinatie/
   ```

3. **Sincronizarea și ștergerea fișierelor vechi:**
   ```bash
   rsync -av --delete /cale/catre/sursa/ /cale/catre/destinatie/
   ```

4. **Sincronizarea cu compresie:**
   ```bash
   rsync -avz /cale/catre/sursa/ utilizator@server:/cale/catre/destinatie/
   ```

## Tips
- Asigurați-vă că utilizați opțiunea `-n` (simulare) pentru a verifica ce fișiere vor fi transferate fără a efectua efectiv transferul.
- Folosiți `--exclude` pentru a exclude anumite fișiere sau directoare din sincronizare.
- Verificați întotdeauna permisiunile fișierelor după transfer, mai ales când lucrați cu servere remote.