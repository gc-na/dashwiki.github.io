# [Română] Debian Almquist Shell (dash) pgrep: Căutare procese după nume

## Overview
Comanda `pgrep` este utilizată pentru a căuta procese pe baza numelui sau a altor atribute. Aceasta returnează ID-urile proceselor (PID) care corespund criteriilor specificate, facilitând gestionarea și monitorizarea proceselor active.

## Usage
Sintaxa de bază a comenzii `pgrep` este următoarea:

```bash
pgrep [opțiuni] [argumente]
```

## Common Options
- `-u, --user`: Caută procesele care aparțin unui anumit utilizator.
- `-f, --full`: Caută în întreaga linie de comandă, nu doar în numele procesului.
- `-n, --newest`: Returnează doar cel mai recent proces care se potrivește.
- `-o, --oldest`: Returnează doar cel mai vechi proces care se potrivește.

## Common Examples
1. Căutarea proceselor cu un nume specific:
   ```bash
   pgrep firefox
   ```

2. Căutarea proceselor care aparțin unui anumit utilizator:
   ```bash
   pgrep -u username
   ```

3. Căutarea proceselor folosind o expresie regulată:
   ```bash
   pgrep -f 'python.*script.py'
   ```

4. Obținerea celui mai recent proces care se potrivește:
   ```bash
   pgrep -n ssh
   ```

5. Obținerea celui mai vechi proces care se potrivește:
   ```bash
   pgrep -o apache2
   ```

## Tips
- Folosiți opțiunea `-f` pentru a căuta procese care nu au nume exacte, dar care pot fi identificate prin argumentele lor.
- Combinați `pgrep` cu comanda `kill` pentru a termina procesele găsite:
  ```bash
  kill $(pgrep firefox)
  ```
- Verificați periodic procesele active folosind `pgrep` pentru a menține sistemul curat și eficient.