# [Debian] Debian Almquist Shell (dash) at: Programarea execuției comenzii

## Overview
Comanda `at` permite utilizatorilor să programeze execuția unor comenzi sau scripturi la o dată și oră specificate în viitor. Aceasta este utilă pentru sarcini automate care trebuie să fie efectuate la momente precise.

## Usage
Sintaxa de bază a comenzii `at` este următoarea:

```
at [opțiuni] [argumente]
```

## Common Options
- `-f FILE`: Specifică un fișier care conține comanda de executat.
- `-m`: Trimite un e-mail utilizatorului după ce comanda a fost executată.
- `-q QUEUE`: Specifică coada de execuție pentru comenzi.
- `-l`: Listează toate sarcinile programate.
- `-d JOB_ID`: Șterge sarcina specificată prin ID-ul jobului.

## Common Examples
1. **Programarea unei comenzi simple**:
   Pentru a rula comanda `echo "Hello, World!"` la ora 15:00, folosiți:
   ```bash
   echo "echo 'Hello, World!'" | at 15:00
   ```

2. **Programarea unui script**:
   Dacă aveți un script numit `backup.sh` pe care doriți să-l rulați la ora 2:30 AM:
   ```bash
   at 2:30 AM -f backup.sh
   ```

3. **Listarea sarcinilor programate**:
   Pentru a vedea toate sarcinile programate:
   ```bash
   at -l
   ```

4. **Ștergerea unei sarcini programate**:
   Dacă doriți să ștergeți o sarcină cu ID-ul 5:
   ```bash
   at -d 5
   ```

## Tips
- Asigurați-vă că aveți permisiuni corespunzătoare pentru a rula comenzi programate.
- Utilizați opțiunea `-m` pentru a primi notificări prin e-mail după ce sarcina a fost executată.
- Verificați periodic sarcinile programate cu `at -l` pentru a evita suprasarcina.