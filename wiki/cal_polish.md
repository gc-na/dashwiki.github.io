# [Polski] Debian Almquist Shell (dash) cal <Użycie: wyświetlanie kalendarza>

## Przegląd
Polecenie `cal` służy do wyświetlania kalendarza w terminalu. Umożliwia przeglądanie miesięcy i lat, a także wyświetlanie dni tygodnia.

## Użycie
Podstawowa składnia polecenia `cal` jest następująca:

```bash
cal [opcje] [argumenty]
```

## Częste opcje
- `-m` - Wyświetla kalendarz w formacie miesięcznym.
- `-y` - Wyświetla kalendarz na cały rok.
- `-3` - Wyświetla kalendarz bieżącego miesiąca oraz miesiąca poprzedniego i następnego.
- `-j` - Wyświetla dni roku (numeracja Julian).
- `-h` - Wyświetla kalendarz w formacie "przyjaznym dla oka".

## Częste przykłady
1. Wyświetlenie kalendarza na bieżący miesiąc:
   ```bash
   cal
   ```

2. Wyświetlenie kalendarza na cały rok:
   ```bash
   cal -y
   ```

3. Wyświetlenie kalendarza dla konkretnego miesiąca i roku (np. grudzień 2023):
   ```bash
   cal 12 2023
   ```

4. Wyświetlenie kalendarza dla trzech miesięcy:
   ```bash
   cal -3
   ```

5. Wyświetlenie kalendarza z numeracją Julian:
   ```bash
   cal -j
   ```

## Wskazówki
- Używaj opcji `-m`, aby uzyskać bardziej przejrzysty widok kalendarza.
- Możesz łączyć różne opcje, aby dostosować wyświetlany kalendarz do swoich potrzeb.
- Sprawdzaj daty ważnych wydarzeń, korzystając z opcji wyświetlania konkretnego miesiąca i roku.