# [Debian] Utilizatori Debian Almquist Shell (dash): Afișează utilizatorii activi

## Overview
Comanda `users` în shell-ul Almquist Debian (dash) este utilizată pentru a afișa numele utilizatorilor care sunt conectați în prezent la sistem. Aceasta oferă o modalitate rapidă de a verifica cine este activ pe mașina respectivă.

## Usage
Sintaxa de bază a comenzii `users` este următoarea:

```bash
users [opțiuni] [argumente]
```

## Common Options
- `-a`: Afișează utilizatorii în mod agregat, adică va include utilizatorii care s-au conectat în sesiuni multiple.
- `-H`: Afișează numele complet al utilizatorilor, dacă este disponibil.

## Common Examples
1. **Afișarea utilizatorilor conectați**:
   ```bash
   users
   ```

2. **Afișarea utilizatorilor conectați în mod agregat**:
   ```bash
   users -a
   ```

3. **Afișarea numelui complet al utilizatorilor**:
   ```bash
   users -H
   ```

## Tips
- Utilizați comanda `who` pentru a obține informații suplimentare despre utilizatorii conectați, cum ar fi ora conectării și terminalul utilizat.
- Comanda `users` este utilă în scripturi pentru a verifica rapid cine este activ, fără a necesita informații detaliate.