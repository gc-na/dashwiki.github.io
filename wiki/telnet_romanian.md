# [Linux] Debian Almquist Shell (dash) telnet utilizare: Conectare la un server prin protocolul Telnet

## Overview
Comanda `telnet` este un client de rețea care permite utilizatorilor să se conecteze la un server prin protocolul Telnet. Aceasta este utilizată pentru a comunica cu servere la distanță, permițând accesul la interfețe de linie de comandă ale acestora.

## Usage
Sintaxa de bază a comenzii `telnet` este următoarea:

```bash
telnet [opțiuni] [hostname] [port]
```

## Common Options
- `-l user`: Specifică numele de utilizator pentru autentificare.
- `-d`: Activează modul de depanare.
- `-n file`: Redirecționează ieșirea de debug către un fișier specificat.
- `-e char`: Specifică un caracter de terminare pentru comenzi.

## Common Examples
1. **Conectare la un server pe portul 23 (portul standard pentru Telnet)**:
   ```bash
   telnet example.com
   ```

2. **Conectare la un server specificând un port diferit**:
   ```bash
   telnet example.com 8080
   ```

3. **Conectare cu un nume de utilizator specificat**:
   ```bash
   telnet -l user example.com
   ```

4. **Activarea modului de depanare**:
   ```bash
   telnet -d example.com
   ```

## Tips
- Folosiți Telnet doar pe rețele de încredere, deoarece datele nu sunt criptate.
- Verificați dacă serverul la care doriți să vă conectați acceptă conexiuni Telnet.
- Luați în considerare utilizarea SSH pentru conexiuni mai sigure, deoarece Telnet transmite informațiile în text clar.