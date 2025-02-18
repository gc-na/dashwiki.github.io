# [Debian] Debian Almquist Shell (dash) date: Afișează data și ora curentă

## Overview
Comanda `date` este utilizată pentru a afișa sau a seta data și ora curentă a sistemului. Aceasta poate fi folosită pentru a obține informații despre timpul curent sau pentru a formata datele într-un mod specific.

## Usage
Sintaxa de bază a comenzii este următoarea:
```
date [opțiuni] [argumente]
```

## Common Options
- `-u`: Afișează data și ora în format UTC (Coordinated Universal Time).
- `+FORMAT`: Permite personalizarea formatului în care este afișată data și ora. De exemplu, `+%Y-%m-%d` va afișa anul, luna și ziua.
- `-d STRING`: Afișează data și ora pentru un anumit șir de caractere, cum ar fi "next Friday".

## Common Examples
1. Afișarea datei și orei curente:
   ```bash
   date
   ```

2. Afișarea datei și orei în format UTC:
   ```bash
   date -u
   ```

3. Afișarea datei într-un format personalizat:
   ```bash
   date "+%Y-%m-%d %H:%M:%S"
   ```

4. Afișarea datei pentru o zi specifică:
   ```bash
   date -d "next Monday"
   ```

5. Afișarea datei în formatul "Zi-Lună-An":
   ```bash
   date "+%d-%m-%Y"
   ```

## Tips
- Folosiți opțiunea `+FORMAT` pentru a adapta afișarea datei și orei conform nevoilor dvs.
- Verificați întotdeauna fusul orar al sistemului pentru a evita confuziile, mai ales când lucrați cu date și ore în diferite locații.
- Comanda `date` poate fi utilă în scripturi pentru a înregistra timpii de execuție sau pentru a crea nume de fișiere bazate pe dată.