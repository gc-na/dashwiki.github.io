# [România] Debian Almquist Shell (dash) hostname utilizare: Afișează sau setează numele gazdelor

## Overview
Comanda `hostname` este utilizată pentru a afișa sau a seta numele gazdelor sistemului. Acest nume este important pentru identificarea sistemului într-o rețea.

## Usage
Sintaxa de bază a comenzii este următoarea:

```bash
hostname [opțiuni] [argumente]
```

## Common Options
- `-f`, `--fqdn`: Afișează numele complet al gazdei (Fully Qualified Domain Name).
- `-i`, `--ip-address`: Afișează adresa IP a gazdei.
- `-s`, `--short`: Afișează doar numele scurt al gazdei.
- `-V`, `--version`: Afișează informații despre versiunea comenzii.

## Common Examples
1. **Afișarea numelui gazdei curente:**
   ```bash
   hostname
   ```

2. **Afișarea numelui complet al gazdei:**
   ```bash
   hostname -f
   ```

3. **Afișarea adresei IP a gazdei:**
   ```bash
   hostname -i
   ```

4. **Setarea unui nou nume gazdă:**
   ```bash
   sudo hostname noul-nume
   ```

5. **Afișarea numelui scurt al gazdei:**
   ```bash
   hostname -s
   ```

## Tips
- Asigurați-vă că aveți permisiuni de administrator atunci când schimbați numele gazdei.
- După schimbarea numelui gazdei, este recomandat să reporniți sistemul pentru a aplica modificările.
- Verificați fișierul `/etc/hostname` pentru a vă asigura că numele gazdei este setat corect la pornirea sistemului.