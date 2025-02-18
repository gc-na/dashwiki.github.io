# [Debian] Debian Almquist Shell (dash) cal utilizare: Afișează un calendar

## Overview
Comanda `cal` este utilizată pentru a afișa un calendar pe terminal. Aceasta poate arăta calendarul pentru luna curentă, pentru o anumită lună sau pentru un an întreg, oferind o modalitate rapidă de a verifica datele.

## Usage
Sintaxa de bază a comenzii `cal` este următoarea:

```bash
cal [opțiuni] [argumente]
```

## Common Options
- `-m`: Afișează calendarul pentru luna curentă.
- `-y`: Afișează calendarul pentru întregul an curent.
- `-3`: Afișează calendarul pentru luna curentă și lunile anterioare și următoare.
- `-j`: Afișează zilele anului (numărul zilei în an).
- `-w`: Afișează săptămânile cu începutul duminicii.

## Common Examples
1. Afișarea calendarului pentru luna curentă:
   ```bash
   cal
   ```

2. Afișarea calendarului pentru o anumită lună și an (de exemplu, martie 2024):
   ```bash
   cal 03 2024
   ```

3. Afișarea calendarului pentru întregul an curent:
   ```bash
   cal -y
   ```

4. Afișarea calendarului pentru luna curentă și lunile anterioare și următoare:
   ```bash
   cal -3
   ```

5. Afișarea calendarului cu zilele anului:
   ```bash
   cal -j
   ```

## Tips
- Folosiți opțiunea `-m` pentru a obține rapid calendarul lunii curente fără a specifica alte argumente.
- Combinați opțiunile pentru a personaliza afișarea calendarului, de exemplu, `cal -3 -j` pentru a vedea calendarul cu numerele zilelor anului.
- Verificați documentația completă a comenzii `cal` folosind `man cal` pentru a descoperi mai multe opțiuni și funcționalități.