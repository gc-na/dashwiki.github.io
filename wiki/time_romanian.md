# [Debian] Debian Almquist Shell (dash) time utilizare: Măsurarea timpului de execuție al unui program

## Overview
Comanda `time` este utilizată pentru a măsura timpul de execuție al unui program sau al unei comenzi. Aceasta oferă informații despre timpul total consumat, timpul utilizat de CPU și timpul de așteptare.

## Usage
Sintaxa de bază a comenzii `time` este următoarea:

```bash
time [options] [arguments]
```

## Common Options
- `-p`: Afișează rezultatele într-un format simplu, compatibil cu POSIX.
- `-o <file>`: Scrie rezultatele în fișierul specificat.
- `-v`: Afișează informații detaliate despre execuția comenzii.

## Common Examples
1. Măsurarea timpului de execuție al unei comenzi simple:
   ```bash
   time ls -l
   ```

2. Salvarea rezultatelor într-un fișier:
   ```bash
   time -o rezultat.txt sleep 2
   ```

3. Afișarea detaliilor despre execuție:
   ```bash
   time -v find / -name "*.txt"
   ```

4. Măsurarea timpului de execuție al unui script:
   ```bash
   time ./script.sh
   ```

## Tips
- Folosiți opțiunea `-p` pentru a obține un format de ieșire simplu, ușor de citit.
- Dacă doriți să comparați timpii de execuție între diferite comenzi, rulați-le în aceeași sesiune de terminal.
- Fiți atenți la timpii de așteptare, care pot influența rezultatele, mai ales în cazul comenzilor care depind de resurse externe.