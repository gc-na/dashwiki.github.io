# [Polski] Debian Almquist Shell (dash) at: planowanie zadań

## Overview
Polecenie `at` w systemie Unix/Linux służy do planowania jednorazowych zadań, które mają być wykonane w określonym czasie w przyszłości. Umożliwia użytkownikom uruchamianie poleceń lub skryptów w wyznaczonym momencie, co jest przydatne w automatyzacji zadań.

## Usage
Podstawowa składnia polecenia `at` jest następująca:

```bash
at [opcje] [argumenty]
```

## Common Options
- `-f FILE` - Wczytuje polecenia do wykonania z pliku.
- `-m` - Wysyła e-mail z powiadomieniem po zakończeniu zadania.
- `-q QUEUE` - Określa kolejkę, w której zadanie ma być umieszczone.
- `-V` - Wyświetla wersję programu.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `at`:

1. **Zaplanowanie prostego polecenia na jutro o 10:00:**

   ```bash
   echo "echo 'Czas na przerwę!'" | at 10:00 tomorrow
   ```

2. **Uruchomienie skryptu o określonej godzinie:**

   ```bash
   at 15:30 <<< "/path/to/script.sh"
   ```

3. **Wczytanie poleceń z pliku:**

   ```bash
   at -f /path/to/commands.txt 14:00
   ```

4. **Zaplanowanie zadania na konkretne dni:**

   ```bash
   echo "backup.sh" | at 2:00 PM 12/25
   ```

## Tips
- Upewnij się, że masz odpowiednie uprawnienia do uruchamiania poleceń w zaplanowanym czasie.
- Sprawdzaj kolejkę zadań za pomocą polecenia `atq`, aby zobaczyć, jakie zadania zostały zaplanowane.
- Pamiętaj, że zadania zaplanowane za pomocą `at` są jednorazowe i nie będą się powtarzać. Jeśli potrzebujesz cyklicznych zadań, rozważ użycie `cron`.