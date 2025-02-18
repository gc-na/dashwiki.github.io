# [Debian] Debian Almquist Shell (dash) echo użycie: Wyświetlanie tekstu w terminalu

## Overview
Polecenie `echo` w powłoce Debian Almquist Shell (dash) służy do wyświetlania tekstu lub zmiennych w terminalu. Jest to jedno z najprostszych i najczęściej używanych poleceń w skryptach powłoki.

## Usage
Podstawowa składnia polecenia `echo` jest następująca:

```sh
echo [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `echo`:

- `-n`: Nie dodawaj nowej linii na końcu wyjścia.
- `-e`: Włącz interpretację sekwencji ucieczki (np. `\n` dla nowej linii, `\t` dla tabulacji).
- `-E`: Wyłącz interpretację sekwencji ucieczki (domyślne zachowanie).

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `echo`:

1. Wyświetlenie prostego tekstu:
    ```sh
    echo "Witaj, świecie!"
    ```

2. Wyświetlenie tekstu bez nowej linii:
    ```sh
    echo -n "To jest bez nowej linii."
    ```

3. Użycie sekwencji ucieczki do formatowania tekstu:
    ```sh
    echo -e "Pierwsza linia\nDruga linia"
    ```

4. Wyświetlenie zmiennej:
    ```sh
    imie="Jan"
    echo "Cześć, $imie!"
    ```

5. Użycie tabulacji w tekście:
    ```sh
    echo -e "Element1\tElement2\tElement3"
    ```

## Tips
- Używaj opcji `-n`, gdy chcesz kontynuować w tej samej linii, co może być przydatne w skryptach.
- Pamiętaj, że niektóre sekwencje ucieczki mogą nie działać bez opcji `-e`, więc zawsze sprawdzaj, czy są one włączone, jeśli potrzebujesz ich użyć.
- Używaj cudzysłowów do otaczania tekstu, aby uniknąć problemów z interpretacją spacji i specjalnych znaków.