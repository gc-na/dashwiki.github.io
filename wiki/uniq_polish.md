# [Debian] Debian Almquist Shell (dash) uniq użycie: Usuwa duplikaty z pliku

## Overview
Polecenie `uniq` służy do usuwania duplikatów z posortowanej listy linii w pliku lub z wejścia standardowego. Działa na zasadzie porównywania kolejnych linii i wyświetlania tylko unikalnych wpisów.

## Usage
Podstawowa składnia polecenia `uniq` jest następująca:

```bash
uniq [opcje] [argumenty]
```

## Common Options
- `-c`: Liczy wystąpienia każdej unikalnej linii i wyświetla je przed linią.
- `-d`: Wyświetla tylko linie, które są duplikatami.
- `-u`: Wyświetla tylko unikalne linie, które występują tylko raz.
- `-i`: Ignoruje wielkość liter podczas porównywania linii.

## Common Examples
Przykłady użycia polecenia `uniq`:

1. Usunięcie duplikatów z pliku:
    ```bash
    uniq plik.txt
    ```

2. Liczenie wystąpień każdej unikalnej linii:
    ```bash
    uniq -c plik.txt
    ```

3. Wyświetlenie tylko duplikatów:
    ```bash
    uniq -d plik.txt
    ```

4. Wyświetlenie tylko unikalnych linii:
    ```bash
    uniq -u plik.txt
    ```

5. Ignorowanie wielkości liter:
    ```bash
    uniq -i plik.txt
    ```

## Tips
- Upewnij się, że dane są posortowane przed użyciem `uniq`, aby działało poprawnie. Możesz użyć polecenia `sort` przed `uniq`.
- Możesz łączyć opcje, na przykład `uniq -ci`, aby uzyskać liczbę unikalnych linii, ignorując wielkość liter.
- Jeśli chcesz przetwarzać dane z potoku, możesz użyć `echo` lub innego polecenia, które generuje dane, np.:
    ```bash
    echo -e "a\nb\na\nc\nd\nb" | sort | uniq
    ```