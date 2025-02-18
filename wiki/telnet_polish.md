# [Debian] Debian Almquist Shell (dash) telnet użycie: nawiązywanie połączeń sieciowych

## Przegląd
Polecenie `telnet` służy do nawiązywania połączeń zdalnych z innymi komputerami w sieci. Umożliwia użytkownikom komunikację z serwerami poprzez protokół Telnet, co jest przydatne do testowania połączeń oraz zarządzania zdalnymi systemami.

## Użycie
Podstawowa składnia polecenia `telnet` jest następująca:

```bash
telnet [opcje] [adres] [port]
```

## Częste opcje
- `-l [nazwa_użytkownika]`: Umożliwia logowanie się jako określony użytkownik.
- `-d`: Włącza tryb debugowania, co może pomóc w diagnozowaniu problemów z połączeniem.
- `-n [plik]`: Umożliwia zapisanie sesji do określonego pliku.

## Częste przykłady
1. Nawiązanie połączenia z serwerem na porcie 23 (domyślny port Telnet):
   ```bash
   telnet example.com
   ```

2. Nawiązanie połączenia z określonym portem:
   ```bash
   telnet example.com 80
   ```

3. Logowanie się jako inny użytkownik:
   ```bash
   telnet -l user example.com
   ```

4. Włączenie trybu debugowania:
   ```bash
   telnet -d example.com
   ```

## Wskazówki
- Używaj `telnet` głównie do testowania połączeń, ponieważ protokół Telnet nie jest bezpieczny. Zamiast tego, rozważ użycie SSH do zdalnego logowania.
- Zawsze sprawdzaj, czy port, z którym próbujesz się połączyć, jest otwarty na serwerze docelowym.
- Pamiętaj, że niektóre serwery mogą nie obsługiwać protokołu Telnet ze względów bezpieczeństwa.