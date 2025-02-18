# [România] Debian Almquist Shell (dash) pkill utilizare: Opriți procesele după nume

## Overview
Comanda `pkill` este utilizată pentru a termina procesele care corespund unui anumit nume sau model. Aceasta permite utilizatorilor să oprească procesele fără a fi nevoie să le identifice mai întâi PID-ul (Process ID).

## Usage
Sintaxa de bază a comenzii `pkill` este următoarea:

```bash
pkill [opțiuni] [argumente]
```

## Common Options
- `-f`: Caută în linia de comandă completă a procesului.
- `-n`: Oprește doar cel mai recent proces care corespunde criteriilor.
- `-o`: Oprește doar cel mai vechi proces care corespunde criteriilor.
- `-signal`: Specifică semnalul care trebuie trimis procesului (de exemplu, `-9` pentru SIGKILL).

## Common Examples
1. Oprirea unui proces după nume:
   ```bash
   pkill firefox
   ```

2. Oprirea tuturor proceselor care conțin un anumit cuvânt în linia de comandă:
   ```bash
   pkill -f "python script.py"
   ```

3. Oprirea celui mai recent proces care corespunde unui nume:
   ```bash
   pkill -n chrome
   ```

4. Oprirea celui mai vechi proces care corespunde unui nume:
   ```bash
   pkill -o sshd
   ```

5. Trimiterea unui semnal specific pentru a opri un proces:
   ```bash
   pkill -9 nginx
   ```

## Tips
- Folosiți opțiunea `-f` cu precauție, deoarece aceasta va căuta în întreaga linie de comandă, ceea ce poate duce la oprirea unor procese neașteptate.
- Verificați procesele active cu `ps aux` înainte de a folosi `pkill`, pentru a evita terminarea proceselor importante.
- Testați comanda cu opțiunea `-l` pentru a lista semnalele disponibile înainte de a specifica un semnal personalizat.