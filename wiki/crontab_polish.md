# [Polski] Debian Almquist Shell (dash) crontab użycie: Planowanie zadań w systemie

## Overview
Polecenie `crontab` służy do zarządzania zadaniami, które mają być automatycznie wykonywane w określonych odstępach czasu w systemie Linux. Umożliwia użytkownikom planowanie zadań, takich jak uruchamianie skryptów lub programów w regularnych interwałach.

## Usage
Podstawowa składnia polecenia `crontab` jest następująca:

```bash
crontab [opcje] [argumenty]
```

## Common Options
- `-e`: Edytuje bieżący plik crontab dla użytkownika.
- `-l`: Wyświetla zawartość bieżącego pliku crontab.
- `-r`: Usuwa bieżący plik crontab.
- `-i`: Potwierdza usunięcie pliku crontab (używane z opcją `-r`).

## Common Examples
1. **Edytowanie crontab**:
   Aby edytować swój plik crontab, użyj:
   ```bash
   crontab -e
   ```

2. **Wyświetlanie crontab**:
   Aby zobaczyć aktualne zaplanowane zadania, wpisz:
   ```bash
   crontab -l
   ```

3. **Usuwanie crontab**:
   Aby usunąć swój plik crontab, użyj:
   ```bash
   crontab -r
   ```

4. **Planowanie zadania**:
   Aby zaplanować skrypt do uruchomienia codziennie o 2:30 w nocy, dodaj następujący wiersz do pliku crontab:
   ```bash
   30 2 * * * /ścieżka/do/skryptu.sh
   ```

5. **Uruchamianie zadania co 5 minut**:
   Aby uruchamiać skrypt co 5 minut, dodaj:
   ```bash
   */5 * * * * /ścieżka/do/skryptu.sh
   ```

## Tips
- Upewnij się, że skrypty mają odpowiednie uprawnienia do wykonywania.
- Zawsze testuj swoje skrypty ręcznie przed dodaniem ich do crontab, aby upewnić się, że działają poprawnie.
- Używaj pełnych ścieżek do plików w skryptach, aby uniknąć problemów z lokalizacją plików.