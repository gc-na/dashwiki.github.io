# [Linux] Debian Almquist Shell (dash) sftp utilizare: Transfer de fișiere prin SSH

## Overview
Comanda `sftp` (SSH File Transfer Protocol) este utilizată pentru a transfera fișiere între un client și un server printr-o conexiune securizată SSH. Aceasta oferă o interfață similară cu comanda `ftp`, dar cu avantajul securității oferite de SSH.

## Usage
Sintaxa de bază a comenzii `sftp` este următoarea:

```bash
sftp [opțiuni] [utilizator@]host
```

## Common Options
Iată câteva opțiuni comune pentru comanda `sftp`:

- `-b file` : Specifică un fișier de comenzi batch care conține comenzi SFTP.
- `-C` : Activează compresia pentru transferurile de fișiere.
- `-i file` : Specifică un fișier de cheie privată pentru autentificare.
- `-o option` : Permite specificarea unor opțiuni SSH suplimentare.
- `-P port` : Specifică un port alternativ pentru conexiunea SSH.

## Common Examples

### Conectare la un server SFTP
Pentru a te conecta la un server SFTP, folosește următoarea comandă:

```bash
sftp utilizator@exemplu.com
```

### Transfer de fișiere de pe client pe server
Pentru a transfera un fișier de pe client pe server, utilizează comanda `put`:

```bash
sftp utilizator@exemplu.com
put fisier.txt
```

### Transfer de fișiere de pe server pe client
Pentru a descărca un fișier de pe server, folosește comanda `get`:

```bash
sftp utilizator@exemplu.com
get fisier.txt
```

### Listarea fișierelor de pe server
Pentru a vizualiza fișierele din directorul curent de pe server, poți folosi comanda `ls`:

```bash
sftp utilizator@exemplu.com
ls
```

### Crearea unui director pe server
Pentru a crea un nou director pe server, folosește comanda `mkdir`:

```bash
sftp utilizator@exemplu.com
mkdir nou_director
```

## Tips
- Asigură-te că ai permisiunile necesare pentru a transfera fișiere pe server.
- Folosește opțiunea `-C` pentru a accelera transferurile de fișiere mari.
- Verifică întotdeauna integritatea fișierelor transferate, mai ales în cazul transferurilor critice.