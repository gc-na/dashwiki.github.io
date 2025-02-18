# [România] Debian Almquist Shell (dash) netcat utilizare: Instrument de rețea pentru transfer de date

## Overview
Comanda `netcat`, adesea denumită "cutter de rețea", este un instrument versatil pentru gestionarea conexiunilor de rețea. Aceasta poate fi utilizată pentru a trimite sau primi date prin intermediul protocoalelor TCP sau UDP, având aplicații variate, de la testarea rețelelor până la transferul de fișiere.

## Usage
Sintaxa de bază a comenzii `netcat` este următoarea:

```bash
netcat [opțiuni] [argumente]
```

## Common Options
- `-l`: Ascultă pentru conexiuni pe un port specificat.
- `-p`: Specifică portul local pe care să asculte sau să se conecteze.
- `-u`: Folosește protocolul UDP în loc de TCP.
- `-v`: Activează modul detaliat, oferind informații suplimentare despre conexiune.
- `-w`: Setează un timeout pentru conexiune, în secunde.

## Common Examples
1. **Ascultarea pe un port specific**:
   ```bash
   netcat -l -p 1234
   ```
   Aceasta va asculta pe portul 1234 pentru conexiuni.

2. **Conectarea la un server**:
   ```bash
   netcat example.com 80
   ```
   Aceasta va stabili o conexiune la serverul `example.com` pe portul 80.

3. **Transfer de fișiere**:
   - Pe mașina care trimite fișierul:
     ```bash
     netcat -l -p 1234 < fisier.txt
     ```
   - Pe mașina care primește fișierul:
     ```bash
     netcat ip_adresa_destinatie 1234 > fisier_recepționat.txt
     ```

4. **Testarea unei conexiuni**:
   ```bash
   netcat -v example.com 22
   ```
   Aceasta va verifica dacă portul 22 al serverului `example.com` este deschis.

## Tips
- Folosește `-v` pentru a obține informații detaliate despre conexiuni, ceea ce poate fi util pentru depanare.
- Asigură-te că firewall-ul nu blochează porturile pe care le folosești cu `netcat`.
- `netcat` poate fi utilizat împreună cu alte comenzi prin pipe, ceea ce îți permite să redirecționezi ieșirea de la o comandă către `netcat` pentru transferuri de date mai complexe.