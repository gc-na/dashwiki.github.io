# [Debian] Debian Almquist Shell (dash) cp utilizare: Copierea fișierelor și directoarelor

## Overview
Comanda `cp` este utilizată pentru a copia fișiere și directoare în sistemul de operare Linux. Aceasta permite utilizatorilor să creeze copii ale fișierelor existente sau să copieze directoare întregi, facilitând gestionarea datelor.

## Usage
Sintaxa de bază a comenzii `cp` este următoarea:

```bash
cp [opțiuni] [sursă] [destinație]
```

## Common Options
- `-r`: Copiază recursiv directoare și conținutul acestora.
- `-i`: Solicita confirmarea înainte de a suprascrie fișierele existente.
- `-u`: Copiază doar fișierele care sunt mai noi decât cele existente în destinație sau care nu există.
- `-v`: Afișează detalii despre fișierele care sunt copiate.

## Common Examples
1. **Copierea unui fișier**:
   ```bash
   cp fisier.txt copie_fisier.txt
   ```

2. **Copierea unui director recursiv**:
   ```bash
   cp -r director_original director_copie
   ```

3. **Copierea cu confirmare**:
   ```bash
   cp -i fisier.txt director_destinatie/
   ```

4. **Copierea fișierelor mai noi**:
   ```bash
   cp -u fisier.txt director_destinatie/
   ```

5. **Afișarea detaliilor în timpul copiei**:
   ```bash
   cp -v fisier.txt director_destinatie/
   ```

## Tips
- Folosiți opțiunea `-i` pentru a evita suprascrierea accidentală a fișierelor existente.
- Când copiați directoare, nu uitați să utilizați opțiunea `-r`.
- Verificați întotdeauna calea de destinație pentru a evita confuziile în gestionarea fișierelor.