# [Polski] Debian Almquist Shell (dash) dig <Użycie: wyszukiwanie informacji o DNS>

## Przegląd
Polecenie `dig` (Domain Information Groper) jest narzędziem służącym do zapytań DNS. Umożliwia użytkownikom uzyskiwanie informacji o rekordach DNS, co jest przydatne w diagnostyce problemów z siecią oraz w administracji serwerami.

## Użycie
Podstawowa składnia polecenia `dig` jest następująca:

```
dig [opcje] [argumenty]
```

## Częste opcje
- `@serwer` - określa serwer DNS, do którego wysyłane jest zapytanie.
- `-t typ` - pozwala na określenie typu rekordu DNS (np. A, MX, CNAME).
- `+short` - wyświetla krótszy wynik, pokazując tylko istotne informacje.
- `+trace` - śledzi zapytanie przez wszystkie serwery DNS, co pozwala zobaczyć, jak zapytanie jest przetwarzane.

## Częste przykłady
1. Aby uzyskać adres IP dla domeny:
   ```bash
   dig example.com
   ```

2. Aby zapytać o rekord MX (Mail Exchange) dla domeny:
   ```bash
   dig example.com -t MX
   ```

3. Aby użyć konkretnego serwera DNS (np. Google):
   ```bash
   dig @8.8.8.8 example.com
   ```

4. Aby uzyskać krótką odpowiedź na zapytanie:
   ```bash
   dig example.com +short
   ```

5. Aby śledzić zapytanie przez wszystkie serwery DNS:
   ```bash
   dig example.com +trace
   ```

## Wskazówki
- Używaj opcji `+short`, aby szybko uzyskać najważniejsze informacje bez zbędnych szczegółów.
- Zawsze sprawdzaj, czy używasz odpowiedniego serwera DNS, zwłaszcza w przypadku problemów z siecią.
- Eksperymentuj z różnymi typami rekordów, aby lepiej zrozumieć, jakie informacje są dostępne dla danej domeny.