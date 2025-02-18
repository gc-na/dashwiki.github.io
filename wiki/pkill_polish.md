# [Debian] Debian Almquist Shell (dash) pkill użycie: Zakończ procesy na podstawie nazwy

## Overview
Polecenie `pkill` w powłoce Debian Almquist Shell (dash) służy do kończenia procesów na podstawie ich nazw lub innych kryteriów. Umożliwia użytkownikom łatwe i szybkie zarządzanie uruchomionymi procesami bez konieczności znajomości ich identyfikatorów PID.

## Usage
Podstawowa składnia polecenia `pkill` jest następująca:

```bash
pkill [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla `pkill`:

- `-f`: Zakończ procesy, których pełne polecenie pasuje do podanego wzorca.
- `-n`: Zakończ najnowszy proces pasujący do wzorca.
- `-o`: Zakończ najstarszy proces pasujący do wzorca.
- `-signal`: Wysyła określony sygnał do procesów (domyślnie jest to SIGTERM).

## Common Examples
Poniżej znajdują się przykłady użycia polecenia `pkill`:

1. Zakończ wszystkie procesy o nazwie `firefox`:

    ```bash
    pkill firefox
    ```

2. Zakończ procesy, których pełna komenda zawiera słowo `python`:

    ```bash
    pkill -f python
    ```

3. Zakończ najnowszy proces o nazwie `nginx`:

    ```bash
    pkill -n nginx
    ```

4. Zakończ najstarszy proces o nazwie `ssh`:

    ```bash
    pkill -o ssh
    ```

5. Wysyłanie sygnału SIGKILL do procesów o nazwie `gedit`:

    ```bash
    pkill -9 gedit
    ```

## Tips
- Używaj opcji `-f` z ostrożnością, ponieważ może zakończyć więcej procesów niż zamierzasz, jeśli wzorzec jest zbyt ogólny.
- Zawsze warto najpierw sprawdzić, jakie procesy zostaną zakończone, używając polecenia `pgrep`, które działa podobnie do `pkill`, ale zamiast kończyć procesy, wyświetla ich identyfikatory.
- Rozważ użycie opcji `-n` lub `-o`, aby precyzyjnie kontrolować, który proces zostanie zakończony, gdy istnieje wiele instancji.