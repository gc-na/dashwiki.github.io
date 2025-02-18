# [România] Debian Almquist Shell (dash) ping utilizare: Verificarea conectivității rețelei

## Overview
Comanda `ping` este utilizată pentru a verifica conectivitatea între două dispozitive de rețea. Aceasta trimite pachete ICMP (Internet Control Message Protocol) către o adresă IP specificată și așteaptă răspunsuri, oferind informații despre latența și pierderile de pachete.

## Usage
Sintaxa de bază a comenzii `ping` este următoarea:

```bash
ping [opțiuni] [argumente]
```

## Common Options
- `-c [număr]`: Specifică numărul de pachete de trimis.
- `-i [secunde]`: Setează intervalul de timp între trimiterile pachetelor.
- `-s [dimensiune]`: Specifică dimensiunea pachetului de date trimis.
- `-t [TTL]`: Setează valoarea Time To Live pentru pachete.

## Common Examples
1. **Ping către un domeniu**:
   ```bash
   ping google.com
   ```

2. **Ping cu un număr specificat de pachete**:
   ```bash
   ping -c 4 google.com
   ```

3. **Ping cu un interval de 2 secunde între pachete**:
   ```bash
   ping -i 2 google.com
   ```

4. **Ping cu dimensiunea pachetului de 1000 de bytes**:
   ```bash
   ping -s 1000 google.com
   ```

5. **Ping cu un TTL specificat**:
   ```bash
   ping -t 64 google.com
   ```

## Tips
- Utilizați opțiunea `-c` pentru a limita numărul de pachete trimise, astfel evitând un ping continuu.
- Verificați latența rețelei prin observarea timpului de răspuns pentru fiecare pachet.
- Folosiți `ping` pentru a diagnostica problemele de conectivitate, cum ar fi pierderile de pachete sau timpii de răspuns mari.