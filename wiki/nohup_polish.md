# [Debian] Debian Almquist Shell (dash) nohup użycie: Uruchamianie procesów w tle

## Overview
Polecenie `nohup` (no hang up) służy do uruchamiania procesów w tle, które nie zostaną przerwane, nawet jeśli użytkownik wyloguje się z systemu. Dzięki temu można kontynuować działanie długoterminowych zadań bez obaw o ich zakończenie.

## Usage
Podstawowa składnia polecenia `nohup` jest następująca:

```bash
nohup [opcje] [argumenty] &
```

Znak `&` na końcu polecenia oznacza, że proces będzie uruchomiony w tle.

## Common Options
- `-h`, `--help`: Wyświetla pomoc i dostępne opcje.
- `-v`, `--version`: Wyświetla wersję programu `nohup`.
- `-o <plik>`: Określa plik, do którego zostaną zapisane standardowe wyjścia (domyślnie jest to `nohup.out`).

## Common Examples
1. Uruchomienie skryptu w tle:
   ```bash
   nohup ./myscript.sh &
   ```

2. Uruchomienie polecenia `ping` w tle i zapisanie wyjścia do pliku:
   ```bash
   nohup ping google.com > ping_output.txt &
   ```

3. Uruchomienie długoterminowego zadania, które nie zostanie przerwane po wylogowaniu:
   ```bash
   nohup tar -czf backup.tar.gz /path/to/directory &
   ```

## Tips
- Używaj `nohup` w połączeniu z `&`, aby uruchomić proces w tle.
- Sprawdzaj plik `nohup.out`, aby zobaczyć standardowe wyjście procesu, jeśli nie określiłeś innego pliku.
- Pamiętaj, że `nohup` nie zatrzymuje procesów, które już działają, więc używaj go przed uruchomieniem długoterminowych zadań.