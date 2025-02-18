# [Linux] Debian Almquist Shell (dash) mtr utilizare: Instrument de diagnosticare a rețelei

## Overview
Comanda `mtr` (My Traceroute) combină funcționalitatea comenzii `ping` și `traceroute`, oferind o analiză detaliată a rutei pe care o urmează pachetele de date către o destinație specificată. Aceasta ajută la diagnosticarea problemelor de rețea și la identificarea întârzierilor sau pierderilor de pachete.

## Usage
Sintaxa de bază a comenzii `mtr` este următoarea:

```bash
mtr [opțiuni] [argumente]
```

## Common Options
- `-r`: Rapoartează rezultatele într-un format de tip raport.
- `-c <număr>`: Specifică numărul de probe de trimis.
- `-i <secunde>`: Setează intervalul de timp între probe.
- `-p`: Afișează porturile utilizate în timpul testului.
- `-w`: Afișează rezultatele într-un format mai prietenos pentru utilizator.

## Common Examples
1. **Testarea unei adrese IP sau a unui domeniu**:
   ```bash
   mtr google.com
   ```

2. **Generarea unui raport cu un număr specific de probe**:
   ```bash
   mtr -r -c 10 google.com
   ```

3. **Testarea unei adrese IP cu interval de 2 secunde între probe**:
   ```bash
   mtr -i 2 8.8.8.8
   ```

4. **Afișarea porturilor utilizate**:
   ```bash
   mtr -p google.com
   ```

5. **Utilizarea formatului prietenos pentru utilizator**:
   ```bash
   mtr -w google.com
   ```

## Tips
- Folosește opțiunea `-r` pentru a obține un raport concis, mai ușor de citit.
- Verifică periodic latența și pierderile de pachete pentru a menține performanța rețelei.
- În cazul în care întâmpini probleme de conectivitate, începe cu comanda `mtr` pentru a identifica rapid unde se află problema.