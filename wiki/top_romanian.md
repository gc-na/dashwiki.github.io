# [Linux] Debian Almquist Shell (dash) top utilizare: Monitorizarea proceselor în timp real

## Overview
Comanda `top` este un instrument esențial în Linux care permite utilizatorilor să monitorizeze procesele active în timp real. Aceasta oferă o vizualizare dinamică a utilizării resurselor sistemului, cum ar fi CPU, memorie și swap, ajutând utilizatorii să identifice procesele care consumă cele mai multe resurse.

## Usage
Sintaxa de bază a comenzii `top` este următoarea:

```bash
top [options] [arguments]
```

## Common Options
Iată câteva opțiuni comune pentru comanda `top`:

- `-d <secunde>`: Setează intervalul de actualizare în secunde.
- `-n <număr>`: Specifică numărul de actualizări pe care `top` le va efectua înainte de a ieși.
- `-u <utilizator>`: Afișează doar procesele aparținând unui anumit utilizator.
- `-p <pid>`: Afișează doar procesele cu ID-ul specificat.

## Common Examples
Iată câteva exemple practice pentru utilizarea comenzii `top`:

1. **Rularea comenzii top**:
   ```bash
   top
   ```

2. **Setarea intervalului de actualizare la 2 secunde**:
   ```bash
   top -d 2
   ```

3. **Afișarea proceselor pentru un anumit utilizator**:
   ```bash
   top -u username
   ```

4. **Afișarea unui singur proces cu un anumit PID**:
   ```bash
   top -p 1234
   ```

5. **Limitarea numărului de actualizări la 5**:
   ```bash
   top -n 5
   ```

## Tips
- Folosește tasta `h` în timpul rulării comenzii `top` pentru a accesa ajutorul și a vedea comenzile rapide disponibile.
- Poți sorta procesele după utilizarea CPU sau memorie apăsând pe tasta `M` sau `P`.
- Pentru a ieși din `top`, apasă `q`. 

Aceste informații te vor ajuta să folosești eficient comanda `top` pentru a monitoriza procesele din sistemul tău.