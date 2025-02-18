# [Debian] Debian Almquist Shell (dash) df utilizare: Afișează informații despre sistemul de fișiere

## Overview
Comanda `df` este utilizată pentru a afișa informații despre utilizarea spațiului pe disc al sistemelor de fișiere montate. Aceasta oferă detalii precum dimensiunea totală, utilizarea curentă și spațiul disponibil pentru fiecare sistem de fișiere.

## Usage
Sintaxa de bază a comenzii `df` este următoarea:

```bash
df [options] [arguments]
```

## Common Options
- `-h`: Afișează dimensiunile într-un format ușor de citit (ex. K, M, G).
- `-T`: Afișează tipul sistemului de fișiere pentru fiecare sistem de fișiere montat.
- `-a`: Include și sistemele de fișiere care nu sunt utilizate.
- `-i`: Afișează informații despre inode-uri în loc de blocuri.

## Common Examples
1. Afișarea informațiilor de bază despre sistemele de fișiere montate:
   ```bash
   df
   ```

2. Afișarea dimensiunilor într-un format ușor de citit:
   ```bash
   df -h
   ```

3. Afișarea tipului sistemului de fișiere:
   ```bash
   df -T
   ```

4. Afișarea informațiilor despre inode-uri:
   ```bash
   df -i
   ```

5. Afișarea informațiilor pentru un sistem de fișiere specific:
   ```bash
   df /home
   ```

## Tips
- Folosiți opțiunea `-h` pentru a face informațiile mai ușor de înțeles, mai ales dacă lucrați cu dimensiuni mari.
- Verificați periodic utilizarea spațiului pe disc pentru a evita problemele de stocare.
- Combinați opțiunile pentru a obține informații mai detaliate, de exemplu, `df -hT` pentru a vedea dimensiunile și tipurile sistemelor de fișiere.