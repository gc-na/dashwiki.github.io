# [România] Debian Almquist Shell (dash) tail utilizare: Afișează ultimele linii ale unui fișier

## Overview
Comanda `tail` este utilizată pentru a afișa ultimele linii ale unui fișier. Este foarte utilă pentru monitorizarea fișierelor de jurnal sau pentru a vizualiza rapid conținutul final al unui fișier mare.

## Usage
Sintaxa de bază a comenzii `tail` este următoarea:

```bash
tail [options] [arguments]
```

## Common Options
- `-n [număr]`: Afișează ultimele `număr` de linii din fișier.
- `-f`: Urmărește în timp real adăugările la fișier, afișând noi linii pe măsură ce sunt scrise.
- `-c [număr]`: Afișează ultimele `număr` de octeți din fișier.

## Common Examples
1. Afișarea ultimelor 10 linii dintr-un fișier:
   ```bash
   tail nume_fisier.txt
   ```

2. Afișarea ultimelor 20 de linii dintr-un fișier:
   ```bash
   tail -n 20 nume_fisier.txt
   ```

3. Urmărirea unui fișier de jurnal în timp real:
   ```bash
   tail -f jurnal.log
   ```

4. Afișarea ultimelor 50 de octeți dintr-un fișier:
   ```bash
   tail -c 50 nume_fisier.txt
   ```

## Tips
- Folosiți opțiunea `-f` pentru a monitoriza fișierele de jurnal, astfel încât să puteți vedea imediat ce se întâmplă.
- Comanda `tail` poate fi combinată cu alte comenzi folosind pipe (`|`) pentru a filtra rezultatele.
- Dacă doriți să salvați ultimele linii într-un alt fișier, puteți redirecționa ieșirea folosind `>`:
   ```bash
   tail -n 10 nume_fisier.txt > ultimele_linii.txt
   ```