# [Polski] Debian Almquist Shell (dash) pgrep: Wyszukiwanie procesów

## Overview
Polecenie `pgrep` służy do wyszukiwania identyfikatorów procesów (PID) na podstawie nazwy procesu lub innych kryteriów. Umożliwia użytkownikom łatwe znajdowanie działających procesów bez potrzeby przeszukiwania całej listy procesów ręcznie.

## Usage
Podstawowa składnia polecenia `pgrep` jest następująca:

```bash
pgrep [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla `pgrep`:

- `-u, --user` - wyszukuje procesy uruchomione przez określonego użytkownika.
- `-f, --full` - wyszukuje pełne polecenie, a nie tylko nazwę procesu.
- `-n, --newest` - zwraca identyfikator najnowszego procesu.
- `-o, --oldest` - zwraca identyfikator najstarszego procesu.
- `-c, --count` - zwraca liczbę procesów, które pasują do kryteriów wyszukiwania.

## Common Examples
Oto kilka praktycznych przykładów użycia `pgrep`:

1. Wyszukiwanie PID procesu o nazwie `bash`:

    ```bash
    pgrep bash
    ```

2. Wyszukiwanie PID procesów uruchomionych przez użytkownika `janek`:

    ```bash
    pgrep -u janek
    ```

3. Wyszukiwanie PID procesu z pełnym poleceniem:

    ```bash
    pgrep -f "python my_script.py"
    ```

4. Liczenie liczby procesów `nginx`:

    ```bash
    pgrep -c nginx
    ```

5. Znalezienie najnowszego procesu `ssh`:

    ```bash
    pgrep -n ssh
    ```

## Tips
- Używaj opcji `-f`, gdy chcesz wyszukiwać według pełnego polecenia, co może być przydatne, gdy masz wiele instancji tego samego programu.
- Możesz łączyć różne opcje, aby uzyskać bardziej precyzyjne wyniki, na przykład `pgrep -u janek -f "python"` znajdzie wszystkie procesy Pythona uruchomione przez użytkownika `janek`.
- Zawsze sprawdzaj, czy masz odpowiednie uprawnienia do przeszukiwania procesów, szczególnie jeśli używasz opcji związanych z innymi użytkownikami.