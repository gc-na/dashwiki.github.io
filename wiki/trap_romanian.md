# [Română] Debian Almquist Shell (dash) trap utilizare: Gestionarea semnalelor în shell

## Overview
Comanda `trap` în shell-ul Debian Almquist (dash) este utilizată pentru a gestiona semnalele și evenimentele care pot afecta execuția unui script. Aceasta permite utilizatorului să definească acțiuni specifice care să fie efectuate atunci când un semnal particular este primit.

## Usage
Sintaxa de bază a comenzii `trap` este următoarea:

```bash
trap [opțiuni] [comandă]
```

## Common Options
- `SIGINT`: Semnalul generat de apăsarea Ctrl+C. Poate fi utilizat pentru a opri un script.
- `SIGTERM`: Semnalul de terminare, folosit pentru a solicita terminarea unui proces.
- `EXIT`: Acest semnal este activat atunci când scriptul se încheie, indiferent de modul în care se termină.

## Common Examples
1. **Capturarea semnalului SIGINT**:
   ```bash
   trap 'echo "Script oprit!"' SIGINT
   while true; do
       echo "Rulează..."
       sleep 1
   done
   ```

2. **Curățarea resurselor la ieșire**:
   ```bash
   trap 'rm -f temp_file; echo "Fișier temporar șters."' EXIT
   touch temp_file
   echo "Lucrez cu fișierul temporar..."
   ```

3. **Gestionarea semnalului SIGTERM**:
   ```bash
   trap 'echo "Terminat cu SIGTERM!"' SIGTERM
   while true; do
       sleep 1
   done
   ```

## Tips
- Este recomandat să folosești `trap` pentru a curăța resursele (de exemplu, fișiere temporare) atunci când scriptul se termină.
- Testează întotdeauna scripturile tale cu semnale pentru a te asigura că se comportă așa cum te aștepți.
- Poți defini mai multe comenzi pentru diferite semnale, separându-le prin spații.