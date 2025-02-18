# [Română] Debian Almquist Shell (dash) dig utilizare: Obține informații DNS

## Overview
Comanda `dig` (Domain Information Groper) este un instrument utilizat pentru a interoga serverele DNS și pentru a obține informații despre numele de domenii, adrese IP și alte date asociate. Este un instrument esențial pentru administrarea rețelelor și pentru depanarea problemelor legate de DNS.

## Usage
Sintaxa de bază a comenzii `dig` este următoarea:

```bash
dig [opțiuni] [argumente]
```

## Common Options
Iată câteva opțiuni comune pentru comanda `dig`:

- `@server` - Specifică serverul DNS pe care doriți să-l interogați.
- `-t type` - Specifică tipul de înregistrare DNS pe care doriți să-l obțineți (de exemplu, A, AAAA, MX).
- `+short` - Afișează rezultatul într-un format mai concis.
- `+trace` - Urmărește calea interogării DNS de la rădăcină până la serverul final.

## Common Examples
Iată câteva exemple practice de utilizare a comenzii `dig`:

1. **Interogarea unei înregistrări A pentru un domeniu:**

   ```bash
   dig example.com
   ```

2. **Interogarea unei înregistrări MX pentru un domeniu:**

   ```bash
   dig -t MX example.com
   ```

3. **Interogarea unui server DNS specific:**

   ```bash
   dig @8.8.8.8 example.com
   ```

4. **Obținerea unei informații scurte despre un domeniu:**

   ```bash
   dig +short example.com
   ```

5. **Urmărirea căii interogării DNS:**

   ```bash
   dig +trace example.com
   ```

## Tips
- Folosiți opțiunea `+short` pentru a obține rezultate mai clare și mai ușor de citit.
- Experimentați cu diferite tipuri de înregistrări DNS pentru a înțelege mai bine structura și funcționarea DNS-ului.
- Verificați periodic serverele DNS pentru a vă asigura că informațiile sunt actualizate și corecte.