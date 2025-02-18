# [Debian] Debian Almquist Shell (dash) who: Afișează utilizatorii conectați

## Overview
Comanda `who` este utilizată pentru a afișa o listă a utilizatorilor care sunt conectați în prezent la sistem. Aceasta oferă informații despre utilizatorii activi, inclusiv numele lor de utilizator, terminalul utilizat și ora la care s-au conectat.

## Usage
Sintaxa de bază a comenzii `who` este următoarea:

```
who [opțiuni] [argumente]
```

## Common Options
- `-b`: Afișează ora la care a fost pornit sistemul.
- `-q`: Afișează doar numele utilizatorilor conectați și numărul total de utilizatori.
- `-H`: Afișează un antet pentru ieșirea standard.

## Common Examples
1. **Afișarea utilizatorilor conectați**:
   ```bash
   who
   ```

2. **Afișarea orei la care a fost pornit sistemul**:
   ```bash
   who -b
   ```

3. **Afișarea doar a numelui utilizatorilor conectați**:
   ```bash
   who -q
   ```

4. **Afișarea utilizatorilor conectați cu antet**:
   ```bash
   who -H
   ```

## Tips
- Utilizați `who` împreună cu comanda `wc -l` pentru a număra utilizatorii conectați:
  ```bash
  who | wc -l
  ```
- Comanda `who` poate fi combinată cu `grep` pentru a căuta un utilizator specific:
  ```bash
  who | grep nume_utilizator
  ```