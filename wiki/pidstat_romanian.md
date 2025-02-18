# [România] Debian Almquist Shell (dash) pidstat utilizare: Monitorizarea statisticilor proceselor

## Overview
Comanda `pidstat` este utilizată pentru a monitoriza statisticile de utilizare a resurselor pentru procesele active. Aceasta oferă informații detaliate despre utilizarea CPU, memorie, I/O și alte metrici relevante pentru fiecare proces în parte.

## Usage
Sintaxa de bază a comenzii `pidstat` este următoarea:

```bash
pidstat [options] [arguments]
```

## Common Options
- `-h`: Afișează ajutorul pentru utilizare.
- `-p <pid>`: Specifică PID-ul procesului pentru care se doresc statisticile.
- `-r`: Afișează utilizarea memoriei.
- `-u`: Afișează utilizarea CPU-ului.
- `-d`: Afișează statisticile de I/O.

## Common Examples
1. **Monitorizarea utilizării CPU pentru toate procesele:**
   ```bash
   pidstat -u
   ```

2. **Monitorizarea utilizării memoriei pentru un proces specific (PID 1234):**
   ```bash
   pidstat -r -p 1234
   ```

3. **Afișarea statisticilor de I/O pentru toate procesele:**
   ```bash
   pidstat -d
   ```

4. **Monitorizarea utilizării CPU la intervale de 2 secunde:**
   ```bash
   pidstat -u 2
   ```

## Tips
- Folosiți opțiunea `-h` pentru a obține ajutor suplimentar și a înțelege mai bine opțiunile disponibile.
- Comanda poate fi combinată cu alte comenzi de monitorizare pentru a obține o imagine de ansamblu mai detaliată a performanței sistemului.
- Monitorizarea periodică a proceselor poate ajuta la identificarea problemelor de performanță înainte ca acestea să devină critice.