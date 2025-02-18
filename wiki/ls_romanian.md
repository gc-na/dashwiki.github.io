# [România] Debian Almquist Shell (dash) ls utilizare: Afișează conținutul directorului

## Overview
Comanda `ls` este utilizată pentru a lista fișierele și directoarele dintr-un director specificat. Aceasta oferă o modalitate rapidă de a vizualiza conținutul unui director, fiind esențială pentru navigarea în sistemul de fișiere.

## Usage
Sintaxa de bază a comenzii `ls` este următoarea:

```bash
ls [opțiuni] [argumente]
```

## Common Options
Iată câteva opțiuni comune pentru comanda `ls`:

- `-l`: Afișează informații detaliate despre fișiere (permisiuni, proprietar, dimensiune, dată).
- `-a`: Include fișierele ascunse (cele care încep cu un punct).
- `-h`: Afișează dimensiunile fișierelor într-un format ușor de citit (ex. KB, MB).
- `-R`: Listează recursiv conținutul subdirectoarelor.
- `-t`: Sortează fișierele după data ultimei modificări.

## Common Examples
Iată câteva exemple practice de utilizare a comenzii `ls`:

1. Listarea fișierelor din directorul curent:
   ```bash
   ls
   ```

2. Listarea fișierelor, inclusiv cele ascunse:
   ```bash
   ls -a
   ```

3. Listarea fișierelor cu detalii complete:
   ```bash
   ls -l
   ```

4. Listarea fișierelor cu dimensiuni ușor de citit:
   ```bash
   ls -lh
   ```

5. Listarea fișierelor dintr-un director specific:
   ```bash
   ls /cale/catre/director
   ```

6. Listarea fișierelor sortate după data ultimei modificări:
   ```bash
   ls -lt
   ```

## Tips
- Folosește `ls -la` pentru a obține o imagine completă a fișierelor, inclusiv cele ascunse și informațiile detaliate.
- Combină opțiunile pentru a personaliza afișarea, de exemplu, `ls -lhR` pentru a lista recursiv cu dimensiuni ușor de citit.
- Utilizează `tab` pentru completarea automată a numelui directorului sau fișierului în linia de comandă, economisind timp și efort.