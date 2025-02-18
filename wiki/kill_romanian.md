# [Linux] Debian Almquist Shell (dash) kill utilizare: Opriți procesele prin semnale

## Overview
Comanda `kill` este utilizată pentru a trimite semnale către procesele în execuție, de obicei pentru a le opri. Deși numele sugerează că aceasta va "ucide" un proces, semnalele pot fi folosite pentru a solicita diferite acțiuni, nu doar oprirea.

## Usage
Sintaxa de bază a comenzii `kill` este următoarea:

```
kill [opțiuni] [argumente]
```

## Common Options
- `-l`: Afișează lista semnalelor disponibile.
- `-s SIGNAL`: Specifică semnalul care trebuie trimis (de exemplu, `SIGTERM`).
- `-n NUMBER`: Trimite semnalul specificat prin numărul său.
- `-p`: Afișează PID-ul procesului fără a trimite semnalul.

## Common Examples
1. Oprirea unui proces folosind PID:
   ```bash
   kill 1234
   ```

2. Oprirea unui proces folosind un semnal specific:
   ```bash
   kill -s SIGKILL 1234
   ```

3. Afișarea semnalelor disponibile:
   ```bash
   kill -l
   ```

4. Trimiterea unui semnal de terminare tuturor proceselor cu un anumit nume:
   ```bash
   killall -s SIGTERM nume_proces
   ```

## Tips
- Verificați PID-ul procesului înainte de a folosi `kill` pentru a evita oprirea proceselor greșite.
- Utilizați `kill -l` pentru a obține o listă completă a semnalelor disponibile și a înțelege ce semnale puteți trimite.
- Folosiți `killall` pentru a opri toate instanțele unui proces specificat, ceea ce poate fi util în gestionarea mai multor procese.