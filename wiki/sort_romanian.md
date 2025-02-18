# [Linux] Debian Almquist Shell (dash) sort utilizare: Sortează liniile din fișiere text

## Overview
Comanda `sort` este utilizată pentru a organiza liniile din fișiere text în ordine alfabetică sau numerică. Aceasta poate fi folosită pentru a sorta datele dintr-un fișier sau pentru a procesa datele dintr-o comandă.

## Usage
Sintaxa de bază a comenzii `sort` este următoarea:

```bash
sort [opțiuni] [argumente]
```

## Common Options
Iată câteva opțiuni comune pentru comanda `sort`:

- `-r`: Sortează în ordine inversă.
- `-n`: Sortează numeric (util pentru numere).
- `-k`: Specifică cheia de sortare (de exemplu, coloana).
- `-u`: Elimină duplicatele din rezultatul sortat.
- `-o`: Scrie rezultatul sortat într-un fișier specificat.

## Common Examples
Iată câteva exemple practice de utilizare a comenzii `sort`:

1. **Sortarea unui fișier text în ordine alfabetică:**
   ```bash
   sort fisier.txt
   ```

2. **Sortarea unui fișier text în ordine inversă:**
   ```bash
   sort -r fisier.txt
   ```

3. **Sortarea numerică a unui fișier:**
   ```bash
   sort -n numere.txt
   ```

4. **Sortarea pe baza unei coloane specifice (de exemplu, a doua coloană):**
   ```bash
   sort -k 2 fisier.txt
   ```

5. **Eliminarea liniilor duplicate și sortarea rezultatelor:**
   ```bash
   sort -u fisier.txt
   ```

6. **Scrierea rezultatelor sortate într-un alt fișier:**
   ```bash
   sort fisier.txt -o fisier_sortat.txt
   ```

## Tips
- Asigurați-vă că datele sunt corect formatate înainte de a le sorta, mai ales când utilizați opțiuni precum `-n`.
- Utilizați opțiunea `-k` pentru a sorta pe baza unor coloane specifice, ceea ce poate fi util în fișierele CSV sau în datele tabelare.
- Combinați `sort` cu alte comenzi, cum ar fi `uniq`, pentru a obține rezultate mai complexe.