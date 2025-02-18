# [Debian] Debian Almquist Shell (dash) scp utilizare: Transferă fișiere între calculatoare

## Overview
Comanda `scp` (secure copy) este utilizată pentru a transfera fișiere între calculatoare printr-o conexiune securizată SSH. Aceasta permite copierea fișierelor local sau de pe un server la un alt server, asigurându-se că datele sunt criptate în timpul transferului.

## Usage
Sintaxa de bază a comenzii `scp` este următoarea:

```bash
scp [opțiuni] [sursă] [destinație]
```

## Common Options
- `-r`: Copiază recursiv directoare.
- `-P`: Specifică un port diferit pentru conexiunea SSH.
- `-i`: Utilizează o cheie privată specificată pentru autentificare.
- `-v`: Activează modul verbose, oferind informații detaliate despre procesul de transfer.

## Common Examples
1. **Transferarea unui fișier de pe calculatorul local pe un server:**
   ```bash
   scp /cale/catre/fișier.txt utilizator@server:/cale/destinatie/
   ```

2. **Transferarea unui fișier de pe un server pe calculatorul local:**
   ```bash
   scp utilizator@server:/cale/catre/fișier.txt /cale/destinatie/
   ```

3. **Transferarea unui director întreg de pe calculatorul local pe un server:**
   ```bash
   scp -r /cale/catre/director utilizator@server:/cale/destinatie/
   ```

4. **Transferarea unui fișier folosind un port specific:**
   ```bash
   scp -P 2222 /cale/catre/fișier.txt utilizator@server:/cale/destinatie/
   ```

## Tips
- Asigurați-vă că aveți permisiunile necesare pentru a accesa fișierele și directoarele pe care doriți să le copiați.
- Utilizați opțiunea `-v` pentru a depista problemele de conectivitate sau autentificare.
- Dacă transferați fișiere mari, luați în considerare utilizarea opțiunii `-C` pentru a activa compresia, ceea ce poate accelera transferul.