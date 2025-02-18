# [Debian] Debian Almquist Shell (dash) diff utilizare: Compararea fișierelor

## Overview
Comanda `diff` este utilizată pentru a compara două fișiere text și a evidenția diferențele dintre ele. Aceasta generează o ieșire care arată ce linii au fost adăugate, șterse sau modificate, facilitând astfel identificarea modificărilor.

## Usage
Sintaxa de bază a comenzii `diff` este următoarea:

```bash
diff [opțiuni] [fișier1] [fișier2]
```

## Common Options
Iată câteva opțiuni comune pentru comanda `diff`:

- `-u`: Afișează ieșirea în format unificat, care este mai ușor de citit.
- `-c`: Afișează ieșirea în format context, oferind mai mult context în jurul modificărilor.
- `-i`: Ignoră diferențele de majuscule și minuscule.
- `-w`: Ignoră diferențele de spațiu alb.

## Common Examples
Iată câteva exemple practice de utilizare a comenzii `diff`:

1. Compararea a două fișiere simple:
   ```bash
   diff fisier1.txt fisier2.txt
   ```

2. Compararea a două fișiere cu ieșire în format unificat:
   ```bash
   diff -u fisier1.txt fisier2.txt
   ```

3. Compararea a două fișiere ignorând diferențele de majuscule și minuscule:
   ```bash
   diff -i fisier1.txt fisier2.txt
   ```

4. Compararea a două directoare:
   ```bash
   diff -r director1/ director2/
   ```

## Tips
- Folosiți opțiunea `-u` pentru a obține o ieșire mai ușor de citit, mai ales atunci când lucrați cu patch-uri.
- Verificați întotdeauna fișierele sursă pentru a evita confuziile în comparații.
- Utilizați `diff` împreună cu comanda `patch` pentru a aplica modificările direct în fișierele sursă.