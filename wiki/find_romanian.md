# [Debian] Debian Almquist Shell (dash) find utilizare: găsirea numelui fișierelor

## Overview
Comanda `find` este utilizată pentru a căuta fișiere și directoare în sistemul de fișiere, pe baza unor criterii specificate de utilizator, cum ar fi numele, dimensiunea, tipul sau data modificării.

## Usage
Sintaxa de bază a comenzii `find` este următoarea:

```bash
find [opțiuni] [argumente]
```

## Common Options
Iată câteva opțiuni comune pentru comanda `find`:

- `-name`: caută fișiere după nume.
- `-type`: specifică tipul de fișier (de exemplu, `f` pentru fișiere obișnuite, `d` pentru directoare).
- `-size`: caută fișiere în funcție de dimensiune.
- `-mtime`: caută fișiere modificate în ultimele n zile.
- `-exec`: execută o comandă pe fiecare fișier găsit.

## Common Examples
Iată câteva exemple practice de utilizare a comenzii `find`:

1. Căutarea unui fișier după nume:
   ```bash
   find /cale/catre/director -name "fisier.txt"
   ```

2. Căutarea tuturor fișierelor de tip director:
   ```bash
   find /cale/catre/director -type d
   ```

3. Căutarea fișierelor mai mari de 1MB:
   ```bash
   find /cale/catre/director -size +1M
   ```

4. Căutarea fișierelor modificate în ultimele 7 zile:
   ```bash
   find /cale/catre/director -mtime -7
   ```

5. Executarea unei comenzi pe fiecare fișier găsit:
   ```bash
   find /cale/catre/director -name "*.log" -exec rm {} \;
   ```

## Tips
- Folosește opțiunea `-iname` pentru a căuta fără a ține cont de majuscule.
- Testează comenzile cu `-print` înainte de a folosi `-exec` pentru a evita ștergerea accidentală a fișierelor.
- Poți combina mai multe criterii de căutare folosind operatori logici precum `-and` sau `-or`.