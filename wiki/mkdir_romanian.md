# [România] Debian Almquist Shell (dash) mkdir utilizare: Crearea de directoare

## Overview
Comanda `mkdir` este utilizată pentru a crea directoare noi în sistemul de fișiere. Aceasta permite utilizatorilor să organizeze fișierele într-o structură ierarhică, facilitând gestionarea acestora.

## Usage
Sintaxa de bază a comenzii `mkdir` este următoarea:

```bash
mkdir [opțiuni] [argumente]
```

## Common Options
- `-p`: Creează directoare părinte, dacă acestea nu există deja.
- `-v`: Afișează un mesaj pentru fiecare director creat.
- `--help`: Afișează informații despre utilizarea comenzii.

## Common Examples
1. Crearea unui singur director:
   ```bash
   mkdir nou_director
   ```

2. Crearea mai multor directoare simultan:
   ```bash
   mkdir director1 director2 director3
   ```

3. Crearea unui director și a subdirectoarelor sale:
   ```bash
   mkdir -p director_principal/subdirector
   ```

4. Crearea unui director și afișarea unui mesaj:
   ```bash
   mkdir -v director_afisat
   ```

## Tips
- Folosiți opțiunea `-p` pentru a evita erorile atunci când creați un director care are un părinte care nu există.
- Verificați întotdeauna permisiunile de scriere în directorul curent pentru a evita problemele la crearea de directoare.
- Utilizați `mkdir` în combinație cu alte comenzi pentru a automatiza procesele de organizare a fișierelor.