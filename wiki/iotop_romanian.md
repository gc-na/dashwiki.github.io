# [Debian] Debian Almquist Shell (dash) iotop utilizare: Monitorizarea utilizării I/O a proceselor

## Overview
Comanda `iotop` este un instrument util pentru monitorizarea utilizării resurselor de intrare/ieșire (I/O) de către procesele care rulează pe sistemul dumneavoastră. Aceasta oferă o interfață similară cu `top`, dar se concentrează pe activitatea I/O, permițând utilizatorilor să identifice procesele care consumă cele mai multe resurse de disc.

## Usage
Sintaxa de bază a comenzii `iotop` este următoarea:

```bash
iotop [options] [arguments]
```

## Common Options
- `-o`, `--only`: Afișează doar procesele care au activitate I/O.
- `-b`, `--batch`: Rulează în modul batch, util pentru redirecționarea ieșirii către un fișier.
- `-n NUM`, `--iterations NUM`: Specifică numărul de iterații pentru care se va rula `iotop`.
- `-d SEC`, `--delay SEC`: Setează intervalul de actualizare în secunde.

## Common Examples
1. **Monitorizarea activității I/O în timp real:**
   ```bash
   iotop
   ```

2. **Afișarea doar a proceselor cu activitate I/O:**
   ```bash
   iotop -o
   ```

3. **Rularea `iotop` în modul batch pentru 10 iterații:**
   ```bash
   iotop -b -n 10
   ```

4. **Setarea unui interval de actualizare de 2 secunde:**
   ```bash
   iotop -d 2
   ```

## Tips
- Utilizați opțiunea `-o` pentru a filtra procesele inactive și a obține o imagine mai clară a utilizării resurselor.
- Rulați `iotop` cu privilegii de administrator (de exemplu, folosind `sudo`) pentru a obține informații complete despre toate procesele.
- În modul batch, redirecționați ieșirea către un fișier pentru a analiza datele ulterioare:
  ```bash
  iotop -b -n 10 > iotop_output.txt
  ```