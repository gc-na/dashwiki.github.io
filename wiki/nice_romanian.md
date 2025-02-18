# [Debian] Debian Almquist Shell (dash) nice utilizare: Modifică prioritatea proceselor

## Overview
Comanda `nice` este utilizată pentru a modifica prioritatea de execuție a proceselor în sistemul de operare Linux. Aceasta permite utilizatorilor să ruleze procese cu o prioritate mai mică sau mai mare, influențând astfel cât de multă resursă de CPU va primi un proces în comparație cu altele.

## Usage
Sintaxa de bază a comenzii `nice` este următoarea:

```bash
nice [opțiuni] [comandă [argumente]]
```

## Common Options
- `-n, --adjustment=N`: Specifică valoarea ajustării priorității. Aceasta poate fi un număr între -20 (prioritate maximă) și 19 (prioritate minimă).
- `-h, --help`: Afișează un mesaj de ajutor și ieșire.
- `--version`: Afișează informații despre versiunea comenzii.

## Common Examples
1. Rularea unei comenzi cu prioritate mai mică:
   ```bash
   nice -n 10 my_script.sh
   ```

2. Rularea unei comenzi cu prioritate mai mare (necesită permisiuni de superutilizator):
   ```bash
   sudo nice -n -5 my_script.sh
   ```

3. Verificarea priorității unui proces existent:
   ```bash
   ps -o pid,ni,cmd -p <PID>
   ```

4. Rularea unui program grafic cu prioritate redusă:
   ```bash
   nice -n 15 gedit
   ```

## Tips
- Utilizați `nice` pentru a evita ca un proces să consume toate resursele CPU, mai ales pe servere sau în medii cu multe aplicații.
- Verificați întotdeauna prioritățile proceselor active folosind comanda `top` sau `htop` pentru a înțelege impactul modificărilor.
- Dacă doriți să modificați prioritatea unui proces deja în execuție, utilizați comanda `renice`.