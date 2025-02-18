# [Polski] Debian Almquist Shell (dash) exit użycie: Zakończenie skryptu lub powrot do powłoki

## Przegląd
Polecenie `exit` w powłoce Debian Almquist Shell (dash) służy do zakończenia bieżącego skryptu lub powrotu do powłoki. Umożliwia ono również zwrócenie kodu zakończenia, który może być użyty do wskazania, czy skrypt zakończył się pomyślnie, czy wystąpił błąd.

## Użycie
Podstawowa składnia polecenia `exit` jest następująca:

```sh
exit [opcje] [argumenty]
```

## Częste opcje
- `n`: Opcjonalny argument, który określa kod zakończenia. Domyślnie jest to 0, co oznacza pomyślne zakończenie.

## Przykłady
Oto kilka praktycznych przykładów użycia polecenia `exit`:

1. Zakończenie skryptu z domyślnym kodem zakończenia (0):

    ```sh
    #!/bin/dash
    echo "Zakończenie skryptu."
    exit
    ```

2. Zakończenie skryptu z kodem zakończenia 1 (błąd):

    ```sh
    #!/bin/dash
    echo "Wystąpił błąd."
    exit 1
    ```

3. Użycie `exit` w interaktywnej powłoce:

    ```sh
    $ exit
    ```

4. Zakończenie skryptu po wykonaniu warunku:

    ```sh
    #!/bin/dash
    if [ ! -f "plik.txt" ]; then
        echo "Plik nie istnieje, kończę skrypt."
        exit 1
    fi
    ```

## Wskazówki
- Używaj `exit` na końcu skryptów, aby jasno określić, czy skrypt zakończył się sukcesem, czy nie.
- Pamiętaj, że kod zakończenia 0 oznacza sukces, a każdy inny kod wskazuje na błąd.
- Możesz sprawdzić kod zakończenia ostatniego polecenia za pomocą zmiennej `$?` w powłoce.