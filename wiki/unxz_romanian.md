# [Linux] Debian Almquist Shell (dash) unxz utilizare: Dezarhivează fișierele comprimate cu extensia .xz

## Overview
Comanda `unxz` este utilizată pentru a dezarhiva fișierele comprimate în format .xz. Aceasta elimină compresia și restabilește fișierul original, permițând utilizatorilor să acceseze conținutul acestuia.

## Usage
Sintaxa de bază a comenzii `unxz` este următoarea:

```bash
unxz [opțiuni] [argumente]
```

## Common Options
- `-k`, `--keep`: Păstrează fișierul comprimat după dezarhivare.
- `-f`, `--force`: Forțează dezarhivarea, suprascriind fișierele existente fără a cere confirmare.
- `-v`, `--verbose`: Afișează informații detaliate în timpul procesului de dezarhivare.

## Common Examples
1. Dezarchivarea unui fișier .xz:
   ```bash
   unxz fisier.xz
   ```

2. Păstrarea fișierului original după dezarhivare:
   ```bash
   unxz -k fisier.xz
   ```

3. Forțarea dezarhivării unui fișier existent:
   ```bash
   unxz -f fisier.xz
   ```

4. Afișarea detaliilor în timpul dezarhivării:
   ```bash
   unxz -v fisier.xz
   ```

## Tips
- Asigurați-vă că aveți suficient spațiu pe disc înainte de a dezarhiva fișiere mari.
- Utilizați opțiunea `-k` dacă doriți să păstrați fișierul comprimat pentru utilizări ulterioare.
- Verificați întotdeauna integritatea fișierului dezarhivat, mai ales dacă a fost descărcat dintr-o sursă externă.