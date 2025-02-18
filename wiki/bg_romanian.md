# [Linux] Debian Almquist Shell (dash) bg: [pune un proces în fundal]

## Overview
Comanda `bg` este utilizată în shell-uri Unix pentru a relua un proces suspendat și a-l muta în fundal. Aceasta permite utilizatorului să continue utilizarea terminalului în timp ce procesul rulează în fundal.

## Usage
Sintaxa de bază a comenzii `bg` este următoarea:

```bash
bg [opțiuni] [argumente]
```

## Common Options
- `job_id`: Specifică identificatorul procesului (job) pe care doriți să-l mutați în fundal. Acesta poate fi un număr sau un prefix `%` urmat de un număr.
- `-l`: Afișează lista proceselor suspendate.

## Common Examples
1. **Mutarea unui proces suspendat în fundal**:
   Dacă aveți un proces suspendat (de exemplu, un editor de text), îl puteți muta în fundal folosind:
   ```bash
   bg %1
   ```

2. **Mutarea ultimului proces suspendat în fundal**:
   Dacă doriți să mutați ultimul proces suspendat în fundal, puteți folosi:
   ```bash
   bg
   ```

3. **Afișarea proceselor suspendate**:
   Pentru a verifica ce procese sunt suspendate, utilizați comanda:
   ```bash
   jobs
   ```

## Tips
- Asigurați-vă că știți ce procese aveți suspendate folosind comanda `jobs` înainte de a utiliza `bg`.
- Puteți combina `bg` cu `disown` pentru a elimina un proces din lista de joburi active, astfel încât să nu mai fie afectat de închiderea terminalului.
- Folosiți `fg` pentru a readuce un proces din fundal în prim-plan, dacă aveți nevoie să interacționați cu el din nou.