# [Debian] Debian Almquist Shell (dash) dstat utilizare: Monitorizarea resurselor sistemului

## Overview
Comanda `dstat` este un instrument puternic utilizat pentru a monitoriza resursele sistemului în timp real. Aceasta combină funcționalitățile mai multor comenzi tradiționale, oferind o vedere de ansamblu asupra utilizării CPU, memoriei, rețelei și a altor resurse.

## Usage
Sintaxa de bază a comenzii `dstat` este următoarea:

```bash
dstat [options] [arguments]
```

## Common Options
Iată câteva opțiuni comune pentru `dstat`, împreună cu explicații scurte:

- `-c` : Afișează utilizarea CPU.
- `-d` : Afișează activitatea discului.
- `-n` : Afișează activitatea rețelei.
- `-m` : Afișează utilizarea memoriei.
- `-t` : Afișează timestamp-uri pentru fiecare linie de ieșire.

## Common Examples
Iată câteva exemple practice de utilizare a comenzii `dstat`:

1. **Monitorizarea utilizării CPU și a activității discului:**

   ```bash
   dstat -c -d
   ```

2. **Afișarea utilizării memoriei și a activității rețelei:**

   ```bash
   dstat -m -n
   ```

3. **Monitorizarea tuturor resurselor cu timestamp-uri:**

   ```bash
   dstat -t -c -d -n -m
   ```

4. **Afișarea statisticilor de rețea cu detalii despre pachete:**

   ```bash
   dstat --net peth0
   ```

## Tips
- Folosiți `dstat` cu opțiuni multiple pentru a obține o imagine de ansamblu completă a performanței sistemului.
- Rulați `dstat` în fundal pentru a monitoriza resursele în timp ce efectuați alte activități.
- Combinați `dstat` cu redirecționarea ieșirii pentru a salva rezultatele într-un fișier pentru analiză ulterioară.