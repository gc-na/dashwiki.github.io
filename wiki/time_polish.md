# [Polski] Debian Almquist Shell (dash) time <Użycie: Mierzenie czasu wykonywania poleceń>

## Przegląd
Polecenie `time` służy do mierzenia czasu wykonania innych poleceń w powłoce. Umożliwia użytkownikom analizowanie wydajności skryptów i programów, dostarczając informacji o czasie rzeczywistym, czasie CPU oraz czasie systemowym.

## Użycie
Podstawowa składnia polecenia `time` jest następująca:

```sh
time [opcje] [argumenty]
```

## Częste opcje
- `-p`: Wyświetla czas w formacie POSIX.
- `-o <plik>`: Zapisuje wyniki do określonego pliku.
- `-v`: Wyświetla szczegółowe informacje o czasie wykonania.

## Częste przykłady
1. Mierzenie czasu wykonania prostego polecenia:
   ```sh
   time ls
   ```

2. Zapisanie wyników do pliku:
   ```sh
   time -o wynik.txt sleep 2
   ```

3. Użycie opcji szczegółowych:
   ```sh
   time -v find / -name "*.txt"
   ```

## Wskazówki
- Używaj opcji `-o`, aby zapisać wyniki do pliku, co ułatwia późniejszą analizę.
- Sprawdzaj różnice w czasie wykonania różnych poleceń, aby zoptymalizować skrypty.
- Pamiętaj, że `time` mierzy czas tylko dla jednego polecenia, więc jeśli chcesz zmierzyć czas dla wielu poleceń, rozważ użycie grupowania w skryptach.