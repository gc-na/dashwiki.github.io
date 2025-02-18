# [Debian] Debian Almquist Shell (dash) xz utilizare: comprimarea fișierelor

## Overview
Comanda `xz` este utilizată pentru a comprima și decomprima fișiere folosind algoritmul de compresie LZMA. Aceasta oferă o rată de compresie foarte bună, fiind ideală pentru reducerea dimensiunii fișierelor mari.

## Usage
Sintaxa de bază a comenzii `xz` este următoarea:

```
xz [options] [arguments]
```

## Common Options
- `-d`, `--decompress`: Decomprimă fișierul specificat.
- `-k`, `--keep`: Păstrează fișierul original după comprimare.
- `-f`, `--force`: Forțează comprimarea, suprascriind fișierele existente.
- `-9`: Utilizează nivelul maxim de compresie.
- `-t`, `--test`: Verifică integritatea fișierului comprimat.

## Common Examples
1. **Comprimarea unui fișier**:
   ```bash
   xz myfile.txt
   ```
   Acest lucru va crea un fișier comprimat numit `myfile.txt.xz`.

2. **Decomprimarea unui fișier**:
   ```bash
   xz -d myfile.txt.xz
   ```
   Aceasta va restaura fișierul original `myfile.txt`.

3. **Comprimarea și păstrarea fișierului original**:
   ```bash
   xz -k myfile.txt
   ```
   Fișierul original va rămâne intact, iar fișierul comprimat va fi creat.

4. **Comprimarea cu nivel maxim**:
   ```bash
   xz -9 myfile.txt
   ```
   Aceasta va utiliza cel mai înalt nivel de compresie disponibil.

5. **Verificarea integrității unui fișier comprimat**:
   ```bash
   xz -t myfile.txt.xz
   ```
   Aceasta va verifica dacă fișierul comprimat este intact.

## Tips
- Folosiți opțiunea `-k` dacă doriți să păstrați fișierele originale după comprimare.
- Verificați întotdeauna integritatea fișierelor comprimate folosind opțiunea `-t` pentru a evita problemele de corupție.
- Experimentați cu diferite niveluri de compresie pentru a găsi un echilibru între dimensiunea fișierului și timpul de procesare.