# [Linux] Debian Almquist Shell (dash) traceroute6 utilizare: Urmărirea rutei IPv6

## Overview
Comanda `traceroute6` este utilizată pentru a urmări calea pe care pachetele de date o parcurg printr-o rețea IPv6. Aceasta ajută la diagnosticarea problemelor de conectivitate și la înțelegerea traseului pe care îl urmează datele pentru a ajunge la o destinație specificată.

## Usage
Sintaxa de bază a comenzii este următoarea:

```bash
traceroute6 [opțiuni] [argumente]
```

## Common Options
Iată câteva opțiuni comune pentru `traceroute6`:

- `-m <max_ttl>`: Specifică valoarea maximă a TTL (Time To Live) pentru pachetele trimise.
- `-p <port>`: Setează portul de destinație pentru probele de traceroute.
- `-w <timeout>`: Definește timpul de așteptare pentru fiecare răspuns.
- `-n`: Afișează adresele IP în loc de numele gazdelor.

## Common Examples
Iată câteva exemple practice de utilizare a comenzii `traceroute6`:

1. Urmărirea rutei către un site web:
   ```bash
   traceroute6 www.example.com
   ```

2. Specificarea unui port de destinație:
   ```bash
   traceroute6 -p 80 www.example.com
   ```

3. Limitarea numărului maxim de hop-uri:
   ```bash
   traceroute6 -m 10 www.example.com
   ```

4. Afișarea adreselor IP fără rezolvarea numelui:
   ```bash
   traceroute6 -n www.example.com
   ```

## Tips
- Asigurați-vă că aveți permisiuni suficiente pentru a rula `traceroute6`, deoarece unele opțiuni pot necesita privilegii de administrator.
- Utilizați opțiunea `-n` pentru a obține rezultate mai rapide, evitând rezolvarea numelui gazdelor.
- Verificați firewall-ul și setările de rețea, deoarece acestea pot afecta rezultatele comenzii `traceroute6`.