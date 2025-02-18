# [Linux] Debian Almquist Shell (dash) gzip utilizare: Compresia fișierelor

## Overview
Comanda `gzip` este utilizată pentru a comprima fișiere, reducându-le dimensiunea pentru a economisi spațiu pe disc. Aceasta folosește algoritmul de compresie DEFLATE, care este eficient și rapid.

## Usage
Sintaxa de bază a comenzii `gzip` este următoarea:

```bash
gzip [options] [arguments]
```

## Common Options
- `-d`, `--decompress`: Decomprimați un fișier gzip.
- `-k`, `--keep`: Păstrați fișierul original după compresie.
- `-v`, `--verbose`: Afișați informații detaliate despre procesul de compresie.
- `-r`, `--recursive`: Comprimați recursiv toate fișierele dintr-un director.

## Common Examples
1. **Compresia unui fișier**:
   ```bash
   gzip fisier.txt
   ```

2. **Decompresia unui fișier**:
   ```bash
   gzip -d fisier.txt.gz
   ```

3. **Păstrarea fișierului original**:
   ```bash
   gzip -k fisier.txt
   ```

4. **Compresia recursivă a fișierelor dintr-un director**:
   ```bash
   gzip -r director/
   ```

5. **Afișarea informațiilor detaliate în timpul compresiei**:
   ```bash
   gzip -v fisier.txt
   ```

## Tips
- Este recomandat să utilizați opțiunea `-k` dacă doriți să păstrați fișierul original pentru referințe ulterioare.
- Verificați dimensiunea fișierelor comprimate folosind comanda `ls -lh` pentru a vedea economiile de spațiu.
- Gzip este cel mai eficient pentru fișiere text, așa că utilizați-l în special pentru documente sau scripturi.