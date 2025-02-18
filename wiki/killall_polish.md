# [Polski] Debian Almquist Shell (dash) killall użycie: Zakończ procesy na podstawie nazwy

## Przegląd
Polecenie `killall` służy do kończenia procesów na podstawie ich nazw. Umożliwia użytkownikom łatwe zarządzanie uruchomionymi aplikacjami, eliminując te, które nie są już potrzebne lub które mogą powodować problemy.

## Użycie
Podstawowa składnia polecenia `killall` wygląda następująco:

```bash
killall [opcje] [argumenty]
```

## Częste opcje
- `-u, --user <użytkownik>`: Zakończ procesy uruchomione przez określonego użytkownika.
- `-q, --quiet`: Nie wyświetlaj komunikatów o błędach, gdy nie ma procesów do zakończenia.
- `-I, --ignore-case`: Ignoruj wielkość liter podczas porównywania nazw procesów.
- `-s, --signal <sygnał>`: Wyślij określony sygnał do procesów (domyślnie jest to SIGTERM).

## Częste przykłady
1. Zakończenie wszystkich procesów o nazwie `firefox`:
   ```bash
   killall firefox
   ```

2. Zakończenie wszystkich procesów uruchomionych przez użytkownika `janek`:
   ```bash
   killall -u janek
   ```

3. Zakończenie procesów z ignorowaniem wielkości liter w nazwie:
   ```bash
   killall -I gedit
   ```

4. Wysłanie sygnału SIGKILL do procesów o nazwie `myapp`:
   ```bash
   killall -s SIGKILL myapp
   ```

## Wskazówki
- Używaj opcji `-q`, aby uniknąć zbędnych komunikatów, gdy nie ma procesów do zakończenia.
- Zawsze upewnij się, że znasz nazwę procesu, który chcesz zakończyć, aby uniknąć przypadkowego zamknięcia ważnych aplikacji.
- Rozważ użycie `killall -I` w przypadku procesów, których nazwy mogą być pisane różnymi literami (np. `MyApp` vs `myapp`).