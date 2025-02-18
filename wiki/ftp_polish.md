# [Debian] Debian Almquist Shell (dash) ftp użycie: Przesyłanie plików przez protokół FTP

## Przegląd
Polecenie `ftp` służy do nawiązywania połączeń z serwerami FTP w celu przesyłania plików. Umożliwia zarówno pobieranie, jak i wysyłanie plików, a także zarządzanie plikami na zdalnym serwerze.

## Użycie
Podstawowa składnia polecenia `ftp` jest następująca:

```bash
ftp [opcje] [argumenty]
```

## Wspólne opcje
- `-i`: Wyłącza tryb interaktywny, co pozwala na przesyłanie plików bez potwierdzenia.
- `-n`: Nie nawiązuje automatycznie połączenia z serwerem po uruchomieniu.
- `-v`: Włącza tryb szczegółowy, wyświetlając więcej informacji o połączeniu.
- `-p`: Umożliwia korzystanie z pasywnego trybu FTP, co jest przydatne w przypadku zapór sieciowych.

## Przykłady
1. Nawiązanie połączenia z serwerem FTP:
   ```bash
   ftp ftp.example.com
   ```

2. Wysłanie pliku na serwer FTP:
   ```bash
   put lokalny_plik.txt
   ```

3. Pobranie pliku z serwera FTP:
   ```bash
   get zdalny_plik.txt
   ```

4. Użycie trybu pasywnego:
   ```bash
   ftp -p ftp.example.com
   ```

5. Wyłączenie trybu interaktywnego podczas przesyłania plików:
   ```bash
   ftp -i ftp.example.com
   put plik_do_wyslania.txt
   ```

## Wskazówki
- Zawsze sprawdzaj, czy masz odpowiednie uprawnienia do przesyłania lub pobierania plików na serwerze FTP.
- Używaj trybu pasywnego, jeśli masz problemy z połączeniem, szczególnie w sieciach z zaporami.
- Regularnie aktualizuj swoje oprogramowanie FTP, aby zapewnić bezpieczeństwo i zgodność z nowymi standardami.