# [Linux] Debian Almquist Shell (dash) uname utilizare: Afișează informații despre sistem

## Overview
Comanda `uname` este utilizată pentru a afișa informații despre sistemul de operare și kernel-ul pe care rulează. Aceasta poate oferi detalii precum numele sistemului, versiunea kernel-ului și tipul arhitecturii hardware.

## Usage
Sintaxa de bază a comenzii `uname` este următoarea:

```bash
uname [options] [arguments]
```

## Common Options
Iată câteva opțiuni comune pentru comanda `uname`, împreună cu explicații scurte:

- `-a`: Afișează toate informațiile disponibile despre sistem.
- `-s`: Afișează numele kernel-ului.
- `-n`: Afișează numele gazdei (hostname).
- `-r`: Afișează versiunea kernel-ului.
- `-v`: Afișează data și ora compilării kernel-ului.
- `-m`: Afișează tipul arhitecturii hardware.
- `-p`: Afișează tipul procesorului (dacă este disponibil).
- `-i`: Afișează informații despre platforma hardware.
- `-o`: Afișează numele sistemului de operare.

## Common Examples
Iată câteva exemple practice ale utilizării comenzii `uname`:

1. Afișarea tuturor informațiilor despre sistem:
   ```bash
   uname -a
   ```

2. Afișarea numelui kernel-ului:
   ```bash
   uname -s
   ```

3. Afișarea versiunii kernel-ului:
   ```bash
   uname -r
   ```

4. Afișarea tipului arhitecturii hardware:
   ```bash
   uname -m
   ```

5. Afișarea numelui gazdei:
   ```bash
   uname -n
   ```

## Tips
- Utilizați opțiunea `-a` pentru a obține o imagine de ansamblu completă a sistemului într-o singură comandă.
- Comanda `uname` poate fi utilă în scripturi pentru a verifica informațiile despre sistem înainte de a rula alte comenzi.
- Verificați frecvent versiunea kernel-ului pentru a vă asigura că aveți cele mai recente actualizări de securitate și funcționalitate.