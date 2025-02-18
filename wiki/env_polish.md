# [Polski] Debian Almquist Shell (dash) env <Użycie: zarządzanie zmiennymi środowiskowymi>

## Przegląd
Polecenie `env` służy do wyświetlania lub modyfikowania zmiennych środowiskowych w systemie. Umożliwia uruchamianie programów w określonym środowisku, co jest przydatne w wielu scenariuszach, takich jak testowanie lub konfigurowanie aplikacji.

## Użycie
Podstawowa składnia polecenia `env` jest następująca:

```bash
env [opcje] [argumenty]
```

## Typowe opcje
- `-i`: Uruchamia program w czystym środowisku, bez żadnych zmiennych środowiskowych.
- `-u VAR`: Usuwa zmienną środowiskową o nazwie VAR przed uruchomieniem programu.
- `VAR=value`: Ustawia zmienną środowiskową VAR na wartość value przed uruchomieniem programu.

## Przykłady
1. Wyświetlenie wszystkich zmiennych środowiskowych:
   ```bash
   env
   ```

2. Uruchomienie programu z określoną zmienną środowiskową:
   ```bash
   env MY_VAR=example_value ./my_script.sh
   ```

3. Uruchomienie programu w czystym środowisku:
   ```bash
   env -i ./my_script.sh
   ```

4. Usunięcie zmiennej środowiskowej przed uruchomieniem programu:
   ```bash
   env -u MY_VAR ./my_script.sh
   ```

## Wskazówki
- Używaj opcji `-i`, gdy chcesz przetestować, jak program działa bez wpływu innych zmiennych środowiskowych.
- Ustawiaj zmienne środowiskowe tylko na czas działania programu, aby uniknąć niezamierzonych zmian w systemie.
- Sprawdzaj zmienne środowiskowe przed ich użyciem, aby upewnić się, że mają odpowiednie wartości.