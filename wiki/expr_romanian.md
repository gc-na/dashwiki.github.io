# [Linux] Debian Almquist Shell (dash) expr utilizare: Evaluarea expresiilor aritmetice și logice

## Overview
Comanda `expr` este utilizată în shell-ul Debian Almquist (dash) pentru a evalua expresii aritmetice, logice și pentru a manipula șiruri de caractere. Aceasta permite utilizatorilor să efectueze calcule simple și să obțină informații din șiruri de text.

## Usage
Sintaxa de bază a comenzii `expr` este următoarea:

```bash
expr [opțiuni] [argumente]
```

## Common Options
- `+` : Adunare.
- `-` : Scădere.
- `*` : Înmulțire (folosiți `\*` pentru a evita confuziile cu wildcard-uri).
- `/` : Împărțire.
- `%` : Restul împărțirii.
- `=` : Comparare pentru egalitate.
- `!=` : Comparare pentru inegalitate.
- `>` : Comparare pentru mai mare.
- `<` : Comparare pentru mai mic.
- `length` : Returnează lungimea unui șir de caractere.

## Common Examples
1. **Adunare a două numere:**
   ```bash
   expr 5 + 3
   ```
   Rezultatul va fi `8`.

2. **Scădere:**
   ```bash
   expr 10 - 4
   ```
   Rezultatul va fi `6`.

3. **Înmulțire:**
   ```bash
   expr 7 \* 6
   ```
   Rezultatul va fi `42`.

4. **Împărțire:**
   ```bash
   expr 20 / 4
   ```
   Rezultatul va fi `5`.

5. **Compararea a două valori:**
   ```bash
   expr 5 = 5
   ```
   Rezultatul va fi `1` (adevărat).

6. **Obținerea lungimii unui șir:**
   ```bash
   expr length "Hello, World!"
   ```
   Rezultatul va fi `13`.

## Tips
- Utilizați ghilimele pentru a încadra șirurile de caractere care conțin spații.
- Fiți atenți la utilizarea caracterului `*`, care trebuie precedat de un backslash (`\`) pentru a evita interpretarea sa ca un wildcard.
- `expr` returnează `0` pentru fals și `1` pentru adevărat în evaluările logice, ceea ce poate fi util în scripturi.