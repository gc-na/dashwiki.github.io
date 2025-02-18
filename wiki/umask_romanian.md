# [Debian] Debian Almquist Shell (dash) umask utilizare: Setarea permisiunilor implicite pentru fișiere

## Overview
Comanda `umask` este utilizată pentru a seta masca de permisiuni implicite pentru fișierele și directoarele create de utilizator. Aceasta determină ce permisiuni vor fi restricționate atunci când se creează un nou fișier sau director.

## Usage
Sintaxa de bază a comenzii `umask` este următoarea:

```bash
umask [opțiuni] [argumente]
```

## Common Options
- `-S`: Afișează masca de permisiuni sub formă simbolică.
- `-p`: Afișează masca de permisiuni curentă, păstrând-o neschimbată.

## Common Examples
1. **Afișarea masca curentă:**
   ```bash
   umask
   ```

2. **Setarea unei masti de permisiuni:**
   ```bash
   umask 027
   ```
   Aceasta va restricționa permisiunile pentru grup și alții, permițând doar utilizatorului să aibă acces complet.

3. **Afișarea masti de permisiuni în format simbolic:**
   ```bash
   umask -S
   ```

4. **Restabilirea valorii implicite a masti:**
   ```bash
   umask 0022
   ```

## Tips
- Este recomandat să verificați masca curentă înainte de a crea fișiere sau directoare pentru a evita problemele de permisiune.
- Puteți adăuga comanda `umask` în fișierul `.bashrc` sau `.profile` pentru a seta automat masca dorită la fiecare sesiune de terminal.
- Fiți atenți la setările de umask, deoarece o mască prea restrictivă poate împiedica accesul altor utilizatori la fișierele dvs.