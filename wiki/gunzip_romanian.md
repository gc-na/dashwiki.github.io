# [Linux] Debian Almquist Shell (dash) gunzip utilizare: Dezarhivează fișierele comprimate

## Overview
Comanda `gunzip` este utilizată pentru a dezarhiva fișierele comprimate în format Gzip. Aceasta elimină extensia `.gz` a fișierului și restabilește fișierul original.

## Usage
Sintaxa de bază a comenzii `gunzip` este următoarea:

```bash
gunzip [opțiuni] [argumente]
```

## Common Options
Iată câteva opțiuni comune pentru `gunzip`:

- `-c`: Scrie fișierul decomprimat pe standard output, fără a modifica fișierul original.
- `-f`: Forțează decomprimarea fișierelor, suprascriind fișierele existente fără a cere confirmare.
- `-k`: Păstrează fișierul comprimat original după decomprimare.
- `-r`: Dezarhivează recursiv fișierele din directoare.

## Common Examples
Iată câteva exemple practice pentru utilizarea comenzii `gunzip`:

1. Dezarhivarea unui fișier simplu:
   ```bash
   gunzip fisier.txt.gz
   ```

2. Dezarhivarea unui fișier și păstrarea originalului:
   ```bash
   gunzip -k fisier.txt.gz
   ```

3. Dezarhivarea fișierului și scrierea pe standard output:
   ```bash
   gunzip -c fisier.txt.gz > fisier_dezarhivat.txt
   ```

4. Dezarhivarea recursivă a tuturor fișierelor `.gz` dintr-un director:
   ```bash
   gunzip -r director/
   ```

## Tips
- Asigurați-vă că aveți permisiuni suficiente pentru a modifica fișierele atunci când utilizați opțiunea `-f`.
- Folosiți opțiunea `-k` dacă doriți să păstrați fișierul comprimat pentru a-l utiliza ulterior.
- Verificați întotdeauna fișierele decomprimate pentru a vă asigura că procesul a fost efectuat corect.