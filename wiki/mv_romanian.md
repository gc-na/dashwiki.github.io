# [Debian] Debian Almquist Shell (dash) mv utilizare: Mută sau redenumește fișiere

## Overview
Comanda `mv` este utilizată în shell-ul Debian Almquist (dash) pentru a muta sau redenumi fișiere și directoare. Aceasta este o comandă esențială pentru gestionarea fișierelor în sistemele de operare bazate pe Unix.

## Usage
Sintaxa de bază a comenzii `mv` este următoarea:

```bash
mv [opțiuni] [sursă] [destinație]
```

## Common Options
Iată câteva opțiuni comune pentru comanda `mv`:

- `-i`: Interactiv; solicită confirmarea înainte de a suprascrie fișierele existente.
- `-u`: Mută doar fișierele care sunt mai noi decât cele existente în destinație sau care nu există.
- `-v`: Afișează numele fișierelor pe măsură ce sunt mutate.

## Common Examples
Iată câteva exemple practice de utilizare a comenzii `mv`:

1. **Mutarea unui fișier într-un alt director:**
   ```bash
   mv document.txt /home/utilizator/documents/
   ```

2. **Redenumirea unui fișier:**
   ```bash
   mv vechi.txt nou.txt
   ```

3. **Mutarea mai multor fișiere într-un director:**
   ```bash
   mv *.jpg /home/utilizator/pictures/
   ```

4. **Utilizarea opțiunii interactive pentru a preveni suprascrierea:**
   ```bash
   mv -i document.txt /home/utilizator/documents/
   ```

5. **Mutarea unui fișier doar dacă este mai nou:**
   ```bash
   mv -u document.txt /home/utilizator/documents/
   ```

## Tips
- Folosiți opțiunea `-i` pentru a evita suprascrierea accidentală a fișierelor importante.
- Verificați întotdeauna calea destinație pentru a vă asigura că mutați fișierele în locul dorit.
- Utilizați `-v` pentru a urmări acțiunile comenzii, mai ales când mutați mai multe fișiere.