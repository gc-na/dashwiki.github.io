# [Debian] Debian Almquist Shell (dash) tee użycie: Zapisuje dane do pliku i wyświetla je na standardowym wyjściu

## Overview
Polecenie `tee` w powłoce Debian Almquist Shell (dash) służy do odczytywania danych ze standardowego wejścia i jednoczesnego zapisywania ich do jednego lub więcej plików. Dzięki temu można jednocześnie przekazywać dane do pliku i wyświetlać je na ekranie.

## Usage
Podstawowa składnia polecenia `tee` wygląda następująco:

```bash
tee [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `tee`:

- `-a` lub `--append`: Dodaje dane do istniejącego pliku zamiast go nadpisywać.
- `-i` lub `--ignore-interrupts`: Ignoruje sygnały przerwania.
- `-p` lub `--output-error`: Określa, jak `tee` ma obsługiwać błędy zapisu.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `tee`:

1. Zapisz dane do pliku i wyświetl je na ekranie:
   ```bash
   echo "Hello, World!" | tee output.txt
   ```

2. Dodaj dane do istniejącego pliku:
   ```bash
   echo "Nowa linia" | tee -a output.txt
   ```

3. Zapisz dane do dwóch plików jednocześnie:
   ```bash
   echo "Dane do plików" | tee file1.txt file2.txt
   ```

4. Użyj `tee` w potoku z innym poleceniem:
   ```bash
   ls -l | tee output.txt | grep "txt"
   ```

## Tips
- Używaj opcji `-a`, gdy chcesz dodać dane do istniejącego pliku, aby nie stracić wcześniejszych informacji.
- Pamiętaj, że `tee` może być używane w potokach, co pozwala na bardziej złożone operacje na danych.
- Sprawdzaj uprawnienia do zapisu w plikach, aby uniknąć błędów podczas używania `tee`.