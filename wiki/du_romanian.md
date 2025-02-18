# [Debian] Debian Almquist Shell (dash) du: măsurarea dimensiunii directorului

## Overview
Comanda `du` (disk usage) este utilizată pentru a estima utilizarea spațiului pe disc a fișierelor și directorilor. Aceasta oferă informații despre cât de mult spațiu ocupă fișierele și subdirectoarele dintr-un director specificat.

## Usage
Sintaxa de bază a comenzii `du` este următoarea:

```bash
du [options] [arguments]
```

## Common Options
- `-h`: Afișează dimensiunile într-un format ușor de citit (ex. KB, MB, GB).
- `-s`: Afișează doar totalul pentru fiecare argument, fără detalii despre subdirectoare.
- `-c`: Afișează un total cumulativ la finalul ieșirii.
- `-a`: Include fișierele în ieșire, nu doar directoarele.
- `--max-depth=N`: Limitează adâncimea de afișare a subdirectoarelor la N niveluri.

## Common Examples
### 1. Măsurarea dimensiunii unui director
Pentru a verifica dimensiunea unui director specific, folosiți:

```bash
du -h /cale/catre/director
```

### 2. Afișarea totalului pentru un director
Dacă doriți să obțineți doar totalul utilizării spațiului pentru un director, utilizați:

```bash
du -sh /cale/catre/director
```

### 3. Afișarea dimensiunii fișierelor și subdirectoarelor
Pentru a vedea dimensiunile fiecărui fișier și subdirector dintr-un director, rulați:

```bash
du -ah /cale/catre/director
```

### 4. Limitarea adâncimii de afișare
Dacă doriți să limitați adâncimea de afișare la 1 nivel, utilizați:

```bash
du -h --max-depth=1 /cale/catre/director
```

### 5. Obținerea unui total cumulativ
Pentru a obține un total cumulativ al dimensiunilor, folosiți:

```bash
du -ch /cale/catre/director/*
```

## Tips
- Utilizați opțiunea `-h` pentru a face ieșirea mai ușor de citit, mai ales când lucrați cu dimensiuni mari.
- Comanda `du` poate fi combinată cu `sort` pentru a ordona rezultatele după dimensiune, de exemplu:

```bash
du -h /cale/catre/director | sort -h
```

- Verificați periodic utilizarea spațiului pe disc pentru a evita problemele de stocare.