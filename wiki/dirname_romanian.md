# [Debian] Debian Almquist Shell (dash) dirname utilizare: Extrage numele directorului dintr-o cale

## Overview
Comanda `dirname` este utilizată pentru a extrage numele directorului dintr-o cale de fișier. Aceasta returnează partea din cale care precede ultimul nume de fișier, permițând utilizatorilor să obțină rapid informații despre structura directorului.

## Usage
Sintaxa de bază a comenzii `dirname` este următoarea:

```bash
dirname [opțiuni] [argumente]
```

## Common Options
- **-z**: Afișează rezultatul utilizând delimitatori null (0-byte) între rezultate, util pentru procesarea în bucle.
- **--help**: Afișează un mesaj de ajutor cu informații despre utilizarea comenzii.
- **--version**: Afișează informații despre versiunea comenzii `dirname`.

## Common Examples
Iată câteva exemple practice de utilizare a comenzii `dirname`:

1. Extrage numele directorului dintr-o cale completă:
   ```bash
   dirname /usr/local/bin/script.sh
   ```
   **Rezultatul:** `/usr/local/bin`

2. Obține numele directorului dintr-o cale relativă:
   ```bash
   dirname ./documente/proiect.txt
   ```
   **Rezultatul:** `./documente`

3. Folosește `dirname` cu mai multe căi:
   ```bash
   dirname /home/user/file1.txt /home/user/file2.txt
   ```
   **Rezultatul:** 
   ```
   /home/user
   /home/user
   ```

4. Afișează numele directorului utilizând opțiunea `-z`:
   ```bash
   dirname -z /var/log/syslog
   ```
   **Rezultatul:** `var/log` (cu un delimitator null la sfârșit)

## Tips
- Folosește `dirname` împreună cu alte comenzi, cum ar fi `basename`, pentru a obține atât numele directorului, cât și numele fișierului dintr-o cale.
- Poți utiliza `dirname` într-un script pentru a manipula căile de fișiere și a organiza fișierele în funcție de directoare.
- Verifică întotdeauna căile pentru a te asigura că sunt corecte înainte de a le folosi în comenzi automate.