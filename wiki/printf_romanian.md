# [Debian] Debian Almquist Shell (dash) printf utilizare: Afișare formatată a textului

## Overview
Comanda `printf` în shell-ul Debian Almquist (dash) este utilizată pentru a afișa text formatat pe ecran. Aceasta permite utilizatorilor să controleze modul în care sunt prezentate datele, inclusiv formatarea numerelor, a stringurilor și a altor tipuri de date.

## Usage
Sintaxa de bază a comenzii `printf` este următoarea:

```
printf [opțiuni] [argumente]
```

## Common Options
- `-v`: Salvează rezultatul în variabila specificată.
- `--help`: Afișează informații despre utilizarea comenzii.
- `--version`: Afișează versiunea comenzii `printf`.

## Common Examples
1. **Afișarea unui text simplu:**
   ```sh
   printf "Salut, lume!\n"
   ```

2. **Formatarea unui număr:**
   ```sh
   printf "Numărul este: %.2f\n" 3.14159
   ```

3. **Afișarea mai multor variabile:**
   ```sh
   nume="Ion"
   varsta=30
   printf "Numele meu este %s și am %d ani.\n" "$nume" "$varsta"
   ```

4. **Afișarea unui tabel:**
   ```sh
   printf "%-10s %-10s\n" "Nume" "Vârstă"
   printf "%-10s %-10d\n" "Ana" 25
   printf "%-10s %-10d\n" "Mihai" 28
   ```

## Tips
- Folosește `\n` pentru a adăuga o nouă linie în textul afișat.
- Poți utiliza formatarea specifică pentru a controla numărul de zecimale afișate la numerele float.
- Verifică întotdeauna sintaxa formatului pentru a evita erorile de afișare.