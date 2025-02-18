# [România] Debian Almquist Shell (dash) head utilizare: afișează primele linii ale unui fișier

## Overview
Comanda `head` este utilizată pentru a afișa primele linii ale unui fișier text. Aceasta este utilă pentru a obține rapid o previzualizare a conținutului unui fișier fără a-l deschide complet.

## Usage
Sintaxa de bază a comenzii `head` este următoarea:

```bash
head [options] [arguments]
```

## Common Options
- `-n NUM` : Afișează primele NUM linii ale fișierului specificat. Dacă NUM nu este specificat, se afișează primele 10 linii.
- `-c NUM` : Afișează primele NUM caractere ale fișierului.
- `-q` : Nu afișează numele fișierului în cazul în care se specifică mai multe fișiere.
- `-v` : Afișează numele fișierului chiar și atunci când este un singur fișier.

## Common Examples
1. Afișarea primelor 10 linii dintr-un fișier:
   ```bash
   head nume_fisier.txt
   ```

2. Afișarea primelor 5 linii dintr-un fișier:
   ```bash
   head -n 5 nume_fisier.txt
   ```

3. Afișarea primelor 20 de caractere dintr-un fișier:
   ```bash
   head -c 20 nume_fisier.txt
   ```

4. Afișarea primelor 10 linii din mai multe fișiere:
   ```bash
   head fisier1.txt fisier2.txt
   ```

5. Afișarea numelui fișierului și a primelor 10 linii:
   ```bash
   head -v nume_fisier.txt
   ```

## Tips
- Folosește `head` împreună cu `tail` pentru a obține o previzualizare a conținutului din mijlocul unui fișier.
- Comanda `head` poate fi combinată cu alte comenzi prin pipe (`|`) pentru a procesa datele. De exemplu, `cat fisier.txt | head -n 5` va afișa primele 5 linii ale fișierului.
- Verifică dimensiunea fișierului înainte de a-l deschide complet, folosind `head`, pentru a decide dacă este relevant să continui cu analiza sa.