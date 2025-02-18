# [Polski] Debian Almquist Shell (dash) ping użycie: Sprawdzanie dostępności hostów w sieci

## Przegląd
Polecenie `ping` służy do sprawdzania dostępności hostów w sieci. Wysyła pakiety ICMP Echo Request do określonego adresu IP lub nazwy hosta i oczekuje na odpowiedzi. Jest to przydatne narzędzie do diagnozowania problemów z połączeniem sieciowym.

## Użycie
Podstawowa składnia polecenia `ping` jest następująca:

```sh
ping [opcje] [argumenty]
```

## Częste opcje
- `-c [liczba]`: Określa liczbę wysyłanych pakietów.
- `-i [czas]`: Ustala czas w sekundach pomiędzy wysyłanymi pakietami.
- `-s [rozmiar]`: Ustala rozmiar wysyłanych pakietów (domyślnie 56 bajtów).
- `-t [TTL]`: Ustala wartość Time To Live dla pakietów.

## Częste przykłady
1. Sprawdzenie dostępności hosta:
   ```sh
   ping example.com
   ```

2. Wysłanie 5 pakietów do hosta:
   ```sh
   ping -c 5 example.com
   ```

3. Ustalenie rozmiaru pakietu na 100 bajtów:
   ```sh
   ping -s 100 example.com
   ```

4. Ustalenie interwału wysyłania pakietów na 2 sekundy:
   ```sh
   ping -i 2 example.com
   ```

5. Ustalenie wartości TTL na 64:
   ```sh
   ping -t 64 example.com
   ```

## Wskazówki
- Używaj opcji `-c`, aby ograniczyć liczbę wysyłanych pakietów, co jest przydatne w testach.
- Monitoruj czas odpowiedzi, aby ocenić jakość połączenia.
- Jeśli ping nie odpowiada, sprawdź, czy host jest aktywny oraz czy nie ma problemów z siecią.