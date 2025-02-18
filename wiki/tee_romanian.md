# [Română] Debian Almquist Shell (dash) tee utilizare: Scrie date în fișiere și pe stdout

## Overview
Comanda `tee` este utilizată pentru a citi din stdin și a scrie simultan atât în stdout, cât și în fișiere. Aceasta permite utilizatorilor să vizualizeze ieșirea unei comenzi în terminal, în timp ce o salvează și într-un fișier.

## Usage
Sintaxa de bază a comenzii este următoarea:
```
tee [opțiuni] [argumente]
```

## Common Options
- `-a`, `--append`: Adaugă ieșirea la sfârșitul fișierului, în loc să-l suprascrie.
- `-i`, `--ignore-interrupts`: Ignoră semnalele de întrerupere.
- `-p`, `--output-error`: Specifică modul de gestionare a erorilor de scriere.

## Common Examples
1. Scrierea ieșirii unei comenzi într-un fișier:
   ```bash
   echo "Salut, lume!" | tee fisier.txt
   ```

2. Adăugarea ieșirii la un fișier existent:
   ```bash
   echo "O nouă linie" | tee -a fisier.txt
   ```

3. Utilizarea `tee` pentru a salva ieșirea unei comenzi complexe:
   ```bash
   ls -l | tee lista_fisiere.txt
   ```

4. Ignorarea semnalelor de întrerupere:
   ```bash
   some_command | tee -i fisier.txt
   ```

## Tips
- Folosiți opțiunea `-a` pentru a evita pierderea datelor existente în fișier.
- Combinați `tee` cu alte comenzi pentru a crea fluxuri de lucru eficiente.
- Verificați întotdeauna permisiunile fișierului pentru a evita erorile de scriere.