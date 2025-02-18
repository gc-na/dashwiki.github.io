# [Linux] Debian Almquist Shell (dash) renice: Modifică prioritatea proceselor

## Overview
Comanda `renice` este utilizată pentru a schimba prioritatea de execuție a proceselor deja în funcțiune. Aceasta permite utilizatorilor să ajusteze prioritatea proceselor, astfel încât să consume mai puține sau mai multe resurse de sistem, în funcție de necesități.

## Usage
Sintaxa de bază a comenzii `renice` este următoarea:

```bash
renice [opțiuni] [argumente]
```

## Common Options
- `-n`, `--priority`: Specifică noua prioritate pentru proces. Valoarea poate fi între -20 (prioritate maximă) și 19 (prioritate minimă).
- `-p`, `--pid`: Indică ID-ul procesului (PID) pentru care se dorește schimbarea priorității.
- `-g`, `--pgroup`: Schimbă prioritatea pentru toate procesele dintr-un grup de procese specificat.
- `-u`, `--user`: Schimbă prioritatea pentru toate procesele aparținând unui utilizator specificat.

## Common Examples
1. Schimbarea priorității unui proces specificat prin PID:
   ```bash
   renice -n 10 -p 1234
   ```

2. Schimbarea priorității tuturor proceselor aparținând unui utilizator:
   ```bash
   renice -n 5 -u username
   ```

3. Schimbarea priorității pentru un grup de procese:
   ```bash
   renice -n -5 -g 5678
   ```

4. Verificarea priorității curente a unui proces:
   ```bash
   ps -o pid,ni,comm -p 1234
   ```

## Tips
- Utilizați valori negative pentru a crește prioritatea unui proces, dar fiți atenți, deoarece procesele cu prioritate mai mare pot afecta performanța sistemului.
- Verificați întotdeauna procesele active și prioritățile lor înainte de a face modificări, pentru a evita interferențele cu procesele critice.
- Este necesar să aveți permisiuni adecvate (de obicei, drepturi de administrator) pentru a schimba prioritatea proceselor care nu vă aparțin.