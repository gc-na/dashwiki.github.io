# [România] Debian Almquist Shell (dash) netstat utilizare: Afișează conexiunile de rețea

## Overview
Comanda `netstat` este un instrument util pentru a vizualiza conexiunile de rețea active, statisticile interfețelor de rețea și diverse informații despre protocoalele de rețea. Aceasta ajută utilizatorii să monitorizeze activitatea rețelei și să depisteze problemele de conectivitate.

## Usage
Sintaxa de bază a comenzii `netstat` este următoarea:

```bash
netstat [opțiuni] [argumente]
```

## Common Options
Iată câteva opțiuni comune pentru comanda `netstat`:

- `-a`: Afișează toate conexiunile și porturile de ascultare.
- `-t`: Afișează conexiunile TCP.
- `-u`: Afișează conexiunile UDP.
- `-l`: Afișează doar porturile de ascultare.
- `-n`: Afișează adresele și numerele de port în format numeric, fără a le rezolva în nume de gazdă.
- `-p`: Afișează identificatorul procesului (PID) și numele programului care utilizează conexiunea.

## Common Examples
Iată câteva exemple practice de utilizare a comenzii `netstat`:

1. **Afișarea tuturor conexiunilor active:**
   ```bash
   netstat -a
   ```

2. **Afișarea conexiunilor TCP:**
   ```bash
   netstat -t
   ```

3. **Afișarea porturilor de ascultare:**
   ```bash
   netstat -l
   ```

4. **Afișarea conexiunilor UDP:**
   ```bash
   netstat -u
   ```

5. **Afișarea conexiunilor cu PID-uri:**
   ```bash
   netstat -p
   ```

6. **Afișarea tuturor conexiunilor în format numeric:**
   ```bash
   netstat -n
   ```

## Tips
- Folosiți opțiunea `-p` pentru a identifica aplicațiile care utilizează anumite conexiuni, ceea ce poate fi util pentru diagnosticarea problemelor.
- Combinați opțiunile pentru a obține informații mai detaliate, de exemplu, `netstat -tuln` pentru a vedea toate conexiunile TCP și UDP în format numeric.
- Rulați comanda periodic pentru a monitoriza schimbările în activitatea rețelei, mai ales în medii de producție.