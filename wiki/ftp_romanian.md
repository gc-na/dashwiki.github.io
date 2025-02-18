# [Linux] Debian Almquist Shell (dash) ftp utilizare: Transfer de fișiere prin protocol FTP

## Overview
Comanda `ftp` este utilizată pentru a transfera fișiere între un client și un server prin intermediul protocolului File Transfer Protocol (FTP). Aceasta permite utilizatorilor să se conecteze la un server FTP, să navigheze prin directoare și să transfere fișiere.

## Usage
Sintaxa de bază a comenzii `ftp` este următoarea:

```
ftp [opțiuni] [argumente]
```

## Common Options
Iată câteva opțiuni comune pentru comanda `ftp`:

- `-i`: Dezactivează modul interactiv, permițând transferul fișierelor fără a solicita confirmări.
- `-n`: Previne conectarea automată la serverul implicit.
- `-v`: Activează modul verbose, oferind informații suplimentare despre transferurile efectuate.

## Common Examples
Iată câteva exemple practice de utilizare a comenzii `ftp`:

1. **Conectarea la un server FTP:**
   ```bash
   ftp ftp.example.com
   ```

2. **Conectarea la un server FTP fără a solicita un nume de utilizator:**
   ```bash
   ftp -n ftp.example.com
   ```

3. **Transferarea unui fișier de pe client pe server:**
   ```bash
   put fisier.txt
   ```

4. **Descărcarea unui fișier de pe server pe client:**
   ```bash
   get fisier.txt
   ```

5. **Listarea fișierelor din directorul curent de pe server:**
   ```bash
   ls
   ```

## Tips
- Asigurați-vă că aveți permisiuni corespunzătoare pentru a transfera fișiere pe serverul FTP.
- Utilizați opțiunea `-i` pentru a accelera transferurile de fișiere mari, evitând confirmările intermediare.
- Verificați întotdeauna conexiunea la server înainte de a începe transferurile, pentru a evita erorile de conectare.