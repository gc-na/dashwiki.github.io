# [Debian] Debian Almquist Shell (dash) socat utilizare: Instrument de transfer de date

## Overview
Comanda `socat` este un instrument puternic pentru transferul de date între două puncte, fie că este vorba despre fișiere, socket-uri, sau fluxuri de date. Este adesea folosit pentru a crea conexiuni de rețea, a redirecționa date sau a interconecta diferite tipuri de fluxuri.

## Usage
Sintaxa de bază a comenzii `socat` este următoarea:

```bash
socat [opțiuni] [argumente]
```

## Common Options
- `-u`: Utilizează modul neblocant.
- `-v`: Activează modul de verbose, afișând informații suplimentare despre transferul de date.
- `TCP:<host>:<port>`: Specifică o conexiune TCP la un anumit host și port.
- `UDP:<host>:<port>`: Specifică o conexiune UDP la un anumit host și port.
- `FILE:<path>`: Indică un fișier de intrare sau ieșire.

## Common Examples
1. **Transfer de date între două socket-uri TCP:**
   ```bash
   socat TCP-LISTEN:1234,fork TCP:localhost:5678
   ```

2. **Redirecționarea unui fișier către un socket TCP:**
   ```bash
   socat TCP:localhost:1234 FILE:/path/to/file.txt
   ```

3. **Crearea unui server UDP care ascultă pe un port specific:**
   ```bash
   socat UDP-LISTEN:1234,fork -
   ```

4. **Conectarea la un server TCP și redirecționarea ieșirii către un fișier:**
   ```bash
   socat FILE:/path/to/output.txt TCP:example.com:80
   ```

## Tips
- Asigurați-vă că aveți permisiunile necesare pentru a accesa fișierele și porturile pe care le utilizați.
- Utilizați opțiunea `-v` pentru a depista problemele de conectivitate sau pentru a verifica datele transferate.
- Experimentați cu diferite tipuri de fluxuri pentru a înțelege mai bine cum funcționează `socat` în diverse scenarii.