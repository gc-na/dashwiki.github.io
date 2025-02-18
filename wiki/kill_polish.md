# [Polski] Debian Almquist Shell (dash) kill użycie: Zakończ procesy

## Overview
Polecenie `kill` służy do wysyłania sygnałów do procesów działających w systemie. Najczęściej używane jest do zakończenia procesów, które nie odpowiadają lub które użytkownik chce zamknąć.

## Usage
Podstawowa składnia polecenia `kill` jest następująca:

```bash
kill [opcje] [argumenty]
```

## Common Options
- `-l`: Wyświetla listę dostępnych sygnałów.
- `-s SIGNAL`: Wysyła określony sygnał do procesu. Można użyć nazwy sygnału lub jego numeru.
- `-n NUMBER`: Wysyła sygnał o podanym numerze.

## Common Examples
1. Zakończenie procesu po jego identyfikatorze (PID):
   ```bash
   kill 1234
   ```

2. Wysłanie sygnału `SIGTERM` (domyślny) do procesu:
   ```bash
   kill -15 1234
   ```

3. Wysłanie sygnału `SIGKILL`, aby natychmiast zakończyć proces:
   ```bash
   kill -9 1234
   ```

4. Wyświetlenie dostępnych sygnałów:
   ```bash
   kill -l
   ```

5. Wysłanie sygnału `SIGINT` do procesu:
   ```bash
   kill -s SIGINT 1234
   ```

## Tips
- Zawsze staraj się używać sygnału `SIGTERM` przed `SIGKILL`, aby dać procesowi szansę na prawidłowe zakończenie.
- Używaj polecenia `ps` lub `top`, aby znaleźć PID procesów, które chcesz zakończyć.
- Możesz użyć `killall` do zakończenia wszystkich procesów o danej nazwie, co może być bardziej wygodne w niektórych sytuacjach.