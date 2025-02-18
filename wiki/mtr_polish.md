# [Polski] Debian Almquist Shell (dash) mtr użycie: Narzędzie do diagnostyki sieci

## Overview
Polecenie `mtr` (My Traceroute) jest narzędziem służącym do diagnostyki sieci, które łączy funkcje poleceń `traceroute` i `ping`. Umożliwia monitorowanie trasy pakietów do określonego hosta oraz mierzenie opóźnień w sieci.

## Usage
Podstawowa składnia polecenia `mtr` jest następująca:

```bash
mtr [opcje] [argumenty]
```

## Common Options
- `-r`: Uruchamia `mtr` w trybie raportu, co pozwala na wygenerowanie jednorazowego raportu.
- `-c <liczba>`: Określa liczbę wysyłanych pakietów (domyślnie 10).
- `-i <czas>`: Ustala interwał czasowy między wysyłanymi pakietami (w sekundach).
- `-p`: Uruchamia `mtr` w trybie tylko ping, bez śledzenia trasy.
- `-w`: Włącza tryb szerokiego wyjścia, co ułatwia odczyt wyników.

## Common Examples
1. Aby uruchomić `mtr` dla konkretnego hosta, na przykład `google.com`:

    ```bash
    mtr google.com
    ```

2. Aby wygenerować raport z 5 wysłanymi pakietami:

    ```bash
    mtr -r -c 5 google.com
    ```

3. Aby ustawić interwał czasowy na 2 sekundy między pakietami:

    ```bash
    mtr -i 2 google.com
    ```

4. Aby uruchomić `mtr` w trybie tylko ping:

    ```bash
    mtr -p google.com
    ```

5. Aby uzyskać szerokie wyjście:

    ```bash
    mtr -w google.com
    ```

## Tips
- Użyj opcji `-r` do generowania raportów, gdy potrzebujesz zapisać wyniki do analizy.
- W przypadku problemów z połączeniem, zwiększ liczbę pakietów za pomocą opcji `-c`, aby uzyskać dokładniejsze dane.
- Regularne monitorowanie trasy do kluczowych serwerów może pomóc w identyfikacji problemów z siecią.