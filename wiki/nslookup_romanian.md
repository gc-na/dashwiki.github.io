# [Debian] Debian Almquist Shell (dash) nslookup utilizare: Verificarea adreselor DNS

## Overview
Comanda `nslookup` este utilizată pentru a interoga serverele DNS pentru a obține informații despre numele de domenii și adresele IP asociate. Aceasta este o unealtă esențială pentru diagnosticarea problemelor de rețea și pentru verificarea configurațiilor DNS.

## Usage
Sintaxa de bază a comenzii `nslookup` este următoarea:

```
nslookup [opțiuni] [argumente]
```

## Common Options
- `-type=tip`: Specifică tipul de înregistrare DNS pe care doriți să-l căutați (de exemplu, A, MX, TXT).
- `-timeout=sec`: Setează timpul de așteptare pentru răspunsul de la serverul DNS.
- `-retry=num`: Specifică numărul de încercări în cazul în care nu se primește un răspuns.

## Common Examples
1. **Căutarea unei adrese IP pentru un nume de domeniu:**
   ```bash
   nslookup example.com
   ```

2. **Căutarea unei înregistrări MX pentru un domeniu:**
   ```bash
   nslookup -type=MX example.com
   ```

3. **Interogarea unui server DNS specific:**
   ```bash
   nslookup example.com 8.8.8.8
   ```

4. **Verificarea unei înregistrări TXT:**
   ```bash
   nslookup -type=TXT example.com
   ```

## Tips
- Utilizați `nslookup` pentru a verifica rapid dacă un domeniu este configurat corect în DNS.
- Experimentați cu diferite tipuri de înregistrări pentru a obține informații detaliate despre un domeniu.
- Dacă întâmpinați probleme, verificați setările serverului DNS pe care îl utilizați.