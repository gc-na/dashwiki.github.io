# [România] Debian Almquist Shell (dash) wc utilizare: Numără liniile, cuvintele și caracterele din fișiere

## Overview
Comanda `wc` (word count) este utilizată pentru a număra liniile, cuvintele și caracterele din fișierele text. Aceasta este o unealtă utilă pentru a obține rapid statistici despre conținutul fișierelor.

## Usage
Sintaxa de bază a comenzii `wc` este următoarea:

```bash
wc [opțiuni] [argumente]
```

## Common Options
- `-l`: Numără liniile din fișier.
- `-w`: Numără cuvintele din fișier.
- `-c`: Numără caracterele din fișier.
- `-m`: Numără caracterele (inclusiv cele multibyte).
- `-L`: Afișează lungimea celei mai lungi linii.

## Common Examples
1. Numără liniile dintr-un fișier:
   ```bash
   wc -l fisier.txt
   ```

2. Numără cuvintele dintr-un fișier:
   ```bash
   wc -w fisier.txt
   ```

3. Numără caracterele dintr-un fișier:
   ```bash
   wc -c fisier.txt
   ```

4. Obține numărul de linii, cuvinte și caractere dintr-un fișier:
   ```bash
   wc fisier.txt
   ```

5. Numără lungimea celei mai lungi linii dintr-un fișier:
   ```bash
   wc -L fisier.txt
   ```

## Tips
- Poți combina opțiunile pentru a obține mai multe statistici simultan. De exemplu, `wc -lw fisier.txt` va afișa numărul de linii și cuvinte.
- Dacă vrei să numeri conținutul din mai multe fișiere, poți specifica mai multe fișiere în comandă, iar `wc` va afișa rezultatele pentru fiecare fișier în parte.
- Folosește `wc` împreună cu alte comenzi prin pipe pentru a analiza ieșirea altor comenzi. De exemplu, `cat fisier.txt | wc -l` va număra liniile din ieșirea comenzii `cat`.