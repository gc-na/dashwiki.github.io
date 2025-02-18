# [Română] Debian Almquist Shell (dash) ps utilizare: Afișează procesele active

## Overview
Comanda `ps` este utilizată pentru a afișa informații despre procesele active din sistem. Aceasta oferă o imagine de ansamblu a proceselor care rulează, inclusiv ID-ul procesului, utilizatorul care le-a inițiat și utilizarea resurselor.

## Usage
Sintaxa de bază a comenzii `ps` este următoarea:

```bash
ps [opțiuni] [argumente]
```

## Common Options
Iată câteva opțiuni comune pentru comanda `ps`:

- `-e`: Afișează toate procesele.
- `-f`: Oferă o ieșire detaliată, incluzând informații suplimentare despre procese.
- `-u [utilizator]`: Afișează procesele pentru un anumit utilizator.
- `-p [PID]`: Afișează informații despre un proces specific, identificat prin PID (ID-ul procesului).
- `--sort`: Permite sortarea rezultatelor după un anumit criteriu, cum ar fi utilizarea CPU sau memoriei.

## Common Examples
Iată câteva exemple practice ale utilizării comenzii `ps`:

1. Afișarea tuturor proceselor active:
   ```bash
   ps -e
   ```

2. Afișarea proceselor cu informații detaliate:
   ```bash
   ps -ef
   ```

3. Afișarea proceselor pentru un anumit utilizator:
   ```bash
   ps -u username
   ```

4. Afișarea informațiilor despre un proces specific:
   ```bash
   ps -p 1234
   ```

5. Afișarea proceselor sortate după utilizarea CPU:
   ```bash
   ps --sort=-%cpu
   ```

## Tips
- Folosiți `ps aux` pentru a obține o listă completă a proceselor, inclusiv cele care nu sunt asociate cu un terminal.
- Combinați `ps` cu comanda `grep` pentru a căuta un proces specific:
  ```bash
  ps -e | grep nume_proces
  ```
- Utilizați opțiunea `-o` pentru a personaliza coloanele afișate, de exemplu:
  ```bash
  ps -eo pid,comm,%mem,%cpu
  ```