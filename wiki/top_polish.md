# [Debian] Debian Almquist Shell (dash) top użycie: monitorowanie procesów systemowych

## Overview
Polecenie `top` w systemie Linux jest narzędziem do monitorowania procesów działających w systemie. Umożliwia użytkownikowi obserwację, które procesy zużywają najwięcej zasobów, takich jak CPU i pamięć, a także dostarcza informacji o ogólnym stanie systemu.

## Usage
Podstawowa składnia polecenia `top` jest następująca:

```bash
top [opcje]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `top`:

- `-d <czas>`: Ustawia czas odświeżania w sekundach.
- `-n <liczba>`: Określa liczbę iteracji, po których `top` zakończy działanie.
- `-u <użytkownik>`: Filtruje procesy według określonego użytkownika.

## Common Examples
Przykłady użycia polecenia `top`:

1. Uruchomienie `top` z domyślnymi ustawieniami:
   ```bash
   top
   ```

2. Ustawienie czasu odświeżania na 2 sekundy:
   ```bash
   top -d 2
   ```

3. Wyświetlenie procesów tylko dla konkretnego użytkownika:
   ```bash
   top -u janek
   ```

4. Ograniczenie liczby iteracji do 5:
   ```bash
   top -n 5
   ```

## Tips
- Aby zakończyć działanie `top`, naciśnij klawisz `q`.
- Możesz sortować procesy według różnych kryteriów, takich jak użycie CPU lub pamięci, klikając odpowiednie nagłówki w interfejsie `top`.
- Użyj klawiszy `Shift + M` w interfejsie `top`, aby posortować procesy według użycia pamięci.