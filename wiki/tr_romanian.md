# [Linux] Debian Almquist Shell (dash) tr: Transformă caractere

## Overview
Comanda `tr` este utilizată pentru a transforma sau a șterge caractere dintr-un flux de date. Aceasta este adesea folosită pentru a modifica textul, cum ar fi înlocuirea literelor sau eliminarea caracterelor nedorite.

## Usage
Sintaxa de bază a comenzii `tr` este următoarea:

```bash
tr [opțiuni] [argumente]
```

## Common Options
- `-d`: Șterge caracterele specificate.
- `-s`: Reduce secvențele de caractere repetate la un singur caracter.
- `-c`: Inversează setul de caractere specificat, aplicând transformarea asupra caracterelor care nu sunt incluse în set.

## Common Examples
1. **Înlocuirea literelor**:
   Pentru a înlocui literele mici cu litere mari:
   ```bash
   echo "text de test" | tr 'a-z' 'A-Z'
   ```

2. **Ștergerea caracterelor**:
   Pentru a elimina toate caracterele 'a' dintr-un text:
   ```bash
   echo "banana" | tr -d 'a'
   ```

3. **Reducerea secvențelor de caractere**:
   Pentru a reduce spațiile multiple la un singur spațiu:
   ```bash
   echo "Acesta    este   un   test." | tr -s ' '
   ```

4. **Inversarea setului de caractere**:
   Pentru a transforma toate caracterele care nu sunt litere în caractere de tip '-':
   ```bash
   echo "abc123" | tr -c 'a-zA-Z' '-'
   ```

## Tips
- Folosește `tr` împreună cu alte comenzi pentru a procesa fișiere mari sau fluxuri de date.
- Verifică întotdeauna rezultatul comenzii pentru a te asigura că transformările sunt cele dorite.
- `tr` funcționează cel mai bine cu text simplu; pentru formate complexe, ia în considerare utilizarea altor instrumente.