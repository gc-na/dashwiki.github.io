# [Română] Debian Almquist Shell (dash) comm: compararea fișierelor

## Overview
Comanda `comm` este utilizată pentru a compara două fișiere sortate linie cu linie. Aceasta afișează liniile care sunt unice pentru fiecare fișier, precum și liniile comune între cele două fișiere.

## Usage
Sintaxa de bază a comenzii `comm` este următoarea:

```bash
comm [opțiuni] [fișier1] [fișier2]
```

## Common Options
- `-1`: Suprimă liniile unice din fișierul 1.
- `-2`: Suprimă liniile unice din fișierul 2.
- `-3`: Suprimă liniile comune între cele două fișiere.
- `-i`: Ignoră diferențele de caz (majuscule/minuscule) în comparație.
- `-u`: Afișează liniile unice din ambele fișiere.

## Common Examples
1. Compararea a două fișiere și afișarea tuturor liniilor:
   ```bash
   comm fisier1.txt fisier2.txt
   ```

2. Afișarea doar a liniilor unice din primul fișier:
   ```bash
   comm -13 fisier1.txt fisier2.txt
   ```

3. Afișarea liniilor comune între cele două fișiere:
   ```bash
   comm -23 fisier1.txt fisier2.txt
   ```

4. Compararea fișierelor ignorând diferențele de caz:
   ```bash
   comm -i fisier1.txt fisier2.txt
   ```

## Tips
- Asigurați-vă că fișierele sunt sortate înainte de a utiliza `comm`, deoarece comanda funcționează corect doar cu fișiere sortate.
- Utilizați opțiunile `-1`, `-2`, sau `-3` pentru a personaliza ieșirea și a obține informațiile dorite.
- Verificați rezultatele cu comanda `sort` înainte de a le compara, pentru a evita confuziile.