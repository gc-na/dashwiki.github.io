# [Polski] Debian Almquist Shell (dash) ss użycie: wyświetlanie informacji o gniazdach

## Przegląd
Polecenie `ss` służy do wyświetlania informacji o gniazdach w systemie. Umożliwia monitorowanie połączeń sieciowych, zarówno TCP, jak i UDP, oraz dostarcza szczegółowych informacji na temat aktywnych połączeń.

## Użycie
Podstawowa składnia polecenia `ss` jest następująca:

```bash
ss [opcje] [argumenty]
```

## Częste opcje
- `-t` – wyświetla tylko połączenia TCP.
- `-u` – wyświetla tylko połączenia UDP.
- `-l` – pokazuje tylko gniazda nasłuchujące.
- `-p` – wyświetla procesy powiązane z gniazdami.
- `-n` – wyświetla numeryczne adresy i porty zamiast nazw.

## Częste przykłady
1. Wyświetlenie wszystkich aktywnych połączeń TCP:
   ```bash
   ss -t
   ```

2. Wyświetlenie wszystkich gniazd nasłuchujących:
   ```bash
   ss -l
   ```

3. Wyświetlenie połączeń UDP:
   ```bash
   ss -u
   ```

4. Wyświetlenie gniazd z informacjami o procesach:
   ```bash
   ss -p
   ```

5. Wyświetlenie wszystkich połączeń z numerycznymi adresami:
   ```bash
   ss -n
   ```

## Wskazówki
- Używaj opcji `-t` i `-u` razem, aby uzyskać pełny obraz połączeń TCP i UDP.
- Opcja `-p` jest przydatna do identyfikacji procesów, które korzystają z gniazd, co może pomóc w rozwiązywaniu problemów.
- Regularne monitorowanie gniazd może pomóc w wykrywaniu nieautoryzowanych połączeń w systemie.