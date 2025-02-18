# [România] Debian Almquist Shell (dash) ln utilizare: Crearea de linkuri simbolice și hard

## Overview
Comanda `ln` este utilizată pentru a crea linkuri către fișiere. Există două tipuri principale de linkuri: linkuri hard și linkuri simbolice. Linkurile simbolice sunt similare cu scurtăturile, în timp ce linkurile hard sunt legături directe către datele fișierului.

## Usage
Sintaxa de bază a comenzii `ln` este următoarea:

```
ln [opțiuni] [argumente]
```

## Common Options
- `-s`: Creează un link simbolic în loc de un link hard.
- `-f`: Forțează crearea linkului, suprascriind un fișier existent.
- `-n`: Nu urmează linkurile simbolice existente.
- `-v`: Afișează informații detaliate despre operațiune.

## Common Examples
1. **Crearea unui link hard:**
   ```bash
   ln fisier_original.txt link_hard.txt
   ```

2. **Crearea unui link simbolic:**
   ```bash
   ln -s fisier_original.txt link_simbolic.txt
   ```

3. **Forțarea creării unui link:**
   ```bash
   ln -f fisier_original.txt link_hard.txt
   ```

4. **Crearea unui link simbolic cu opțiunea verbose:**
   ```bash
   ln -sv fisier_original.txt link_simbolic.txt
   ```

## Tips
- Folosește linkuri simbolice pentru a crea scurtături către fișiere sau directoare care se află în locații diferite.
- Fii atent la utilizarea opțiunii `-f`, deoarece aceasta va suprascrie fișierele existente fără avertisment.
- Verifică întotdeauna dacă linkurile simbolice funcționează corect, mai ales după mutarea fișierelor originale.