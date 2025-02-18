# [Debian] Debian Almquist Shell (dash) grep utilizare: Căutare de text în fișiere

## Overview
Comanda `grep` este un instrument puternic folosit pentru a căuta și a filtra textul din fișiere. Aceasta permite utilizatorilor să găsească linii care conțin un anumit șir de caractere, fiind extrem de utilă în analiza fișierelor de log sau în procesarea textului.

## Usage
Sintaxa de bază a comenzii `grep` este următoarea:
```bash
grep [opțiuni] [argumente]
```

## Common Options
- `-i`: Ignoră diferențele dintre litere mari și mici.
- `-v`: Afișează liniile care nu conțin șirul specificat.
- `-r`: Caută recursiv în directoare.
- `-n`: Afișează numerele de linie în rezultatele căutării.
- `-l`: Afișează doar numele fișierelor care conțin șirul căutat.

## Common Examples
1. Căutarea unui șir de caractere într-un fișier:
   ```bash
   grep "text_cautat" fisier.txt
   ```

2. Căutarea unui șir de caractere fără a ține cont de majuscule:
   ```bash
   grep -i "text_cautat" fisier.txt
   ```

3. Căutarea recursivă într-un director:
   ```bash
   grep -r "text_cautat" /cale/catre/director/
   ```

4. Afișarea numerelor de linie pentru fiecare rezultat:
   ```bash
   grep -n "text_cautat" fisier.txt
   ```

5. Afișarea fișierelor care conțin un anumit șir:
   ```bash
   grep -l "text_cautat" *.txt
   ```

## Tips
- Folosește opțiunea `-v` pentru a exclude anumite linii din rezultate, ceea ce poate fi util în filtrarea informațiilor.
- Combină `grep` cu alte comenzi prin utilizarea pipe-ului (`|`) pentru a crea comenzi mai complexe.
- Salvează rezultatele căutării într-un fișier folosind redirecționarea (`>`) pentru a le analiza ulterior.