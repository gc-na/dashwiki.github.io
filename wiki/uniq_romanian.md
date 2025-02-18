# [Debian] Debian Almquist Shell (dash) uniq utilizare: Elimină liniile duplicate din fișiere

## Overview
Comanda `uniq` este utilizată pentru a elimina liniile duplicate consecutive dintr-un fișier sau dintr-un flux de date. Aceasta este utilă atunci când doriți să obțineți o listă unică de intrări dintr-un set de date.

## Usage
Sintaxa de bază a comenzii `uniq` este următoarea:

```bash
uniq [opțiuni] [argumente]
```

## Common Options
- `-c`: Numără liniile duplicate și le afișează împreună cu numărul de apariții.
- `-d`: Afișează doar liniile care sunt duplicate.
- `-u`: Afișează doar liniile unice, adică cele care nu au duplicate.
- `-i`: Ignoră diferențele dintre litere mari și mici.

## Common Examples

1. **Eliminarea liniilor duplicate dintr-un fișier:**
   ```bash
   uniq fisier.txt
   ```

2. **Numărarea liniilor duplicate:**
   ```bash
   uniq -c fisier.txt
   ```

3. **Afișarea doar a liniilor duplicate:**
   ```bash
   uniq -d fisier.txt
   ```

4. **Afișarea doar a liniilor unice:**
   ```bash
   uniq -u fisier.txt
   ```

5. **Ignorarea diferențelor de caz:**
   ```bash
   uniq -i fisier.txt
   ```

## Tips
- Asigurați-vă că datele sunt sortate înainte de a utiliza `uniq`, deoarece aceasta elimină doar liniile duplicate consecutive.
- Puteți combina `uniq` cu comanda `sort` pentru a obține o listă unică dintr-un fișier nesortat:
  ```bash
  sort fisier.txt | uniq
  ```
- Folosiți opțiunea `-c` pentru a obține o idee despre frecvența apariției fiecărei linii, ceea ce poate fi util în analiza datelor.