# [Debian] Debian Almquist Shell (dash) cmp utilizare: Compararea fișierelor binare

## Overview
Comanda `cmp` este utilizată pentru a compara două fișiere binare sau textuale, byte cu byte. Aceasta va indica prima diferență găsită între cele două fișiere, oferind informații despre poziția exactă a diferenței.

## Usage
Sintaxa de bază a comenzii `cmp` este următoarea:
```
cmp [opțiuni] [fișier1] [fișier2]
```

## Common Options
- `-l`: Afișează diferențele byte cu byte, inclusiv valorile fiecărui byte diferit.
- `-s`: Nu afișează nimic, dar returnează un cod de ieșire care indică dacă fișierele sunt identice sau nu.
- `-i`: Specifică un offset de la care să înceapă compararea fișierelor.

## Common Examples
1. Compararea a două fișiere:
   ```sh
   cmp fisier1.txt fisier2.txt
   ```

2. Compararea fișierelor și afișarea diferențelor byte cu byte:
   ```sh
   cmp -l fisier1.bin fisier2.bin
   ```

3. Compararea fișierelor fără a afișa ieșiri, doar codul de ieșire:
   ```sh
   cmp -s fisier1.txt fisier2.txt
   ```

4. Compararea fișierelor începând de la un anumit offset:
   ```sh
   cmp -i 10 fisier1.txt fisier2.txt
   ```

## Tips
- Folosiți opțiunea `-s` pentru a verifica rapid dacă două fișiere sunt identice, fără a fi nevoie să vizualizați ieșirile.
- Când comparați fișiere binare mari, opțiunea `-l` poate oferi detalii utile despre diferențele specifice.
- Asigurați-vă că aveți permisiuni suficiente pentru a accesa fișierele pe care doriți să le comparați.