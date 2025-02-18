# [România] Debian Almquist Shell (dash) rmdir utilizare: Șterge directoare goale

## Overview
Comanda `rmdir` este utilizată pentru a șterge directoare goale din sistemul de fișiere. Aceasta este o metodă simplă și eficientă de a curăța structura de directoare, eliminând acele directoare care nu conțin fișiere sau subdirectoare.

## Usage
Sintaxa de bază a comenzii `rmdir` este următoarea:

```bash
rmdir [opțiuni] [argumente]
```

## Common Options
Iată câteva opțiuni comune pentru comanda `rmdir`:

- `--ignore-fail-on-non-empty`: Ignoră erorile dacă directorul nu este gol.
- `--verbose`: Afișează un mesaj pentru fiecare director șters.
- `--help`: Afișează ajutorul pentru utilizarea comenzii.

## Common Examples
Iată câteva exemple practice pentru utilizarea comenzii `rmdir`:

1. **Ștergerea unui director gol:**
   ```bash
   rmdir /cale/catre/director
   ```

2. **Ștergerea mai multor directoare goale simultan:**
   ```bash
   rmdir /cale/catre/director1 /cale/catre/director2
   ```

3. **Afișarea unui mesaj pentru fiecare director șters:**
   ```bash
   rmdir --verbose /cale/catre/director
   ```

4. **Ignorarea erorilor pentru directoare care nu sunt goale:**
   ```bash
   rmdir --ignore-fail-on-non-empty /cale/catre/director
   ```

## Tips
- Asigură-te că directorul pe care dorești să-l ștergi este gol, altfel comanda va eșua.
- Folosește opțiunea `--verbose` pentru a verifica ce directoare au fost șterse cu succes.
- Dacă ai nevoie să ștergi un director care conține fișiere sau subdirectoare, poți folosi comanda `rm -r` în loc de `rmdir`.