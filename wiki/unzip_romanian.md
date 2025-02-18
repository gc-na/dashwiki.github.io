# [România] Debian Almquist Shell (dash) unzip utilizare: Extrage fișiere din arhive ZIP

## Overview
Comanda `unzip` este utilizată pentru a extrage fișiere din arhivele ZIP. Aceasta permite utilizatorilor să acceseze conținutul arhivelor și să le salveze în sistemul de fișiere.

## Usage
Sintaxa de bază a comenzii `unzip` este următoarea:

```bash
unzip [opțiuni] [argumente]
```

## Common Options
- `-l`: Listează conținutul arhivei fără a o extrage.
- `-d [director]`: Specifică directorul în care fișierele extrase vor fi salvate.
- `-o`: Suprascrie fișierele existente fără a solicita confirmarea.
- `-q`: Rulați în modul tăcut, fără a afișa mesaje de progres.

## Common Examples
1. **Extrageți fișierele dintr-o arhivă ZIP:**

   ```bash
   unzip arhiva.zip
   ```

2. **Extrageți fișierele într-un director specific:**

   ```bash
   unzip arhiva.zip -d /cale/catre/director
   ```

3. **Listați conținutul arhivei fără a o extrage:**

   ```bash
   unzip -l arhiva.zip
   ```

4. **Suprascrieți fișierele existente fără confirmare:**

   ```bash
   unzip -o arhiva.zip
   ```

5. **Rulați comanda în modul tăcut:**

   ```bash
   unzip -q arhiva.zip
   ```

## Tips
- Asigurați-vă că aveți permisiuni suficiente pentru a extrage fișierele în directorul dorit.
- Folosiți opțiunea `-d` pentru a organiza fișierele extrase în directoare separate, evitând astfel aglomerarea directorului curent.
- Verificați întotdeauna conținutul arhivei cu `-l` înainte de a o extrage, mai ales dacă nu sunteți sigur de sursa acesteia.