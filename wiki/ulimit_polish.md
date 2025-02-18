# [Polski] Debian Almquist Shell (dash) ulimit użycie: Ustawianie limitów zasobów procesów

## Overview
Polecenie `ulimit` w powłoce Debian Almquist Shell (dash) służy do ustawiania lub wyświetlania limitów zasobów dla procesów uruchamianych w bieżącej powłoce. Dzięki temu można kontrolować, ile zasobów systemowych mogą wykorzystać uruchamiane procesy, co jest szczególnie przydatne w zarządzaniu wydajnością i stabilnością systemu.

## Usage
Podstawowa składnia polecenia `ulimit` jest następująca:

```sh
ulimit [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `ulimit`:

- `-a`: Wyświetla wszystkie aktualne limity zasobów.
- `-c`: Ustawia lub wyświetla limit rozmiaru pliku zrzutu pamięci (core dump).
- `-d`: Ustawia lub wyświetla limit rozmiaru segmentu danych.
- `-f`: Ustawia lub wyświetla limit rozmiaru pliku.
- `-l`: Ustawia lub wyświetla limit rozmiaru pamięci, która może być zablokowana w pamięci.
- `-m`: Ustawia lub wyświetla limit rozmiaru pamięci fizycznej.
- `-n`: Ustawia lub wyświetla limit liczby otwartych plików.
- `-s`: Ustawia lub wyświetla limit rozmiaru stosu.
- `-t`: Ustawia lub wyświetla limit czasu CPU w sekundach.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `ulimit`:

1. Wyświetlenie wszystkich limitów zasobów:
   ```sh
   ulimit -a
   ```

2. Ustawienie limitu liczby otwartych plików na 1024:
   ```sh
   ulimit -n 1024
   ```

3. Ustawienie limitu rozmiaru pliku na 10 MB:
   ```sh
   ulimit -f 10240
   ```

4. Wyświetlenie limitu rozmiaru stosu:
   ```sh
   ulimit -s
   ```

5. Ustawienie limitu czasu CPU na 30 sekund:
   ```sh
   ulimit -t 30
   ```

## Tips
- Używaj `ulimit -a` na początku, aby sprawdzić aktualne limity przed ich modyfikacją.
- Pamiętaj, że zmiany w limitach zasobów są lokalne dla bieżącej powłoki i nie wpływają na inne procesy.
- Ustawiaj limity z rozwagą, aby uniknąć niezamierzonych problemów z wydajnością aplikacji.