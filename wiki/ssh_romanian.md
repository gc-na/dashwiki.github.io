# [Linux] Debian Almquist Shell (dash) ssh utilizare: Conectare la un server prin SSH

## Overview
Comanda `ssh` (Secure Shell) este utilizată pentru a stabili o conexiune securizată la un alt sistem prin rețea. Aceasta permite utilizatorilor să se conecteze la un server la distanță, să execute comenzi și să transfere fișiere într-un mod criptat.

## Usage
Sintaxa de bază a comenzii `ssh` este următoarea:

```bash
ssh [opțiuni] [utilizator@]host
```

## Common Options
- `-p [port]`: Specifică portul pe care se va conecta SSH (implicit este 22).
- `-i [fișier]`: Utilizează un fișier de cheie privată specificat pentru autentificare.
- `-v`: Activează modul verbose, oferind mai multe informații despre procesul de conectare.
- `-X`: Permite redirecționarea X11, permițând rularea aplicațiilor grafice de pe server pe mașina locală.

## Common Examples
1. **Conectare la un server prin SSH**:
   ```bash
   ssh user@hostname
   ```

2. **Conectare la un server pe un port diferit**:
   ```bash
   ssh -p 2222 user@hostname
   ```

3. **Utilizarea unei chei private pentru autentificare**:
   ```bash
   ssh -i ~/.ssh/id_rsa user@hostname
   ```

4. **Activarea modului verbose pentru diagnosticare**:
   ```bash
   ssh -v user@hostname
   ```

5. **Conectare la un server și rularea unei comenzi**:
   ```bash
   ssh user@hostname 'ls -l /var/www'
   ```

## Tips
- Asigurați-vă că utilizați chei SSH pentru o autentificare mai sigură în loc de parole.
- Verificați fișierul `~/.ssh/config` pentru a configura aliasuri și opțiuni specifice pentru diferite servere.
- Utilizați `ssh-agent` pentru a gestiona cheile SSH și a evita introducerea constantă a parolei.