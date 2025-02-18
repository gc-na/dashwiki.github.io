# [România] Debian Almquist Shell (dash) crontab utilizare: Programarea sarcinilor automate

## Overview
Comanda `crontab` este utilizată pentru a programa sarcini automate care se execută la intervale regulate pe un sistem Linux. Aceasta permite utilizatorilor să definească comenzi care să fie rulate automat la anumite momente sau la intervale specificate.

## Usage
Sintaxa de bază a comenzii `crontab` este următoarea:

```bash
crontab [opțiuni] [argumente]
```

## Common Options
- `-e`: Editează crontab-ul utilizatorului curent.
- `-l`: Listează sarcinile programate în crontab-ul utilizatorului curent.
- `-r`: Șterge crontab-ul utilizatorului curent.
- `-i`: Confirmă ștergerea crontab-ului cu un mesaj de avertizare.

## Common Examples
1. **Editarea crontab-ului:**
   Pentru a edita crontab-ul utilizatorului curent, folosiți:
   ```bash
   crontab -e
   ```

2. **Listarea sarcinilor programate:**
   Pentru a vedea sarcinile programate, utilizați:
   ```bash
   crontab -l
   ```

3. **Ștergerea crontab-ului:**
   Pentru a șterge crontab-ul curent, utilizați:
   ```bash
   crontab -r
   ```

4. **Programarea unei sarcini:**
   Pentru a rula un script la fiecare zi la ora 2:00 AM, adăugați următoarea linie în crontab:
   ```bash
   0 2 * * * /cale/catre/script.sh
   ```

5. **Programarea unei sarcini la fiecare 5 minute:**
   Pentru a rula un script la fiecare 5 minute, adăugați:
   ```bash
   */5 * * * * /cale/catre/script.sh
   ```

## Tips
- Asigurați-vă că scripturile pe care le programați au permisiuni de execuție.
- Verificați periodic sarcinile din crontab pentru a evita acumularea de sarcini inutile.
- Utilizați redirecționarea ieșirii pentru a captura erorile sau rezultatele scripturilor, de exemplu:
  ```bash
  0 2 * * * /cale/catre/script.sh >> /cale/catre/log.txt 2>&1
  ```