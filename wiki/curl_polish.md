# [Debian] Debian Almquist Shell (dash) curl użycie: Pobieranie danych z internetu

## Overview
Polecenie `curl` jest narzędziem używanym do przesyłania danych z lub do serwera, korzystającym z różnych protokołów, takich jak HTTP, HTTPS, FTP i wiele innych. Jest to niezwykle przydatne narzędzie do pobierania plików, interakcji z API oraz testowania połączeń sieciowych.

## Usage
Podstawowa składnia polecenia `curl` wygląda następująco:

```bash
curl [opcje] [argumenty]
```

## Common Options
Oto niektóre z najczęściej używanych opcji polecenia `curl`:

- `-O` – pobiera plik i zapisuje go z oryginalną nazwą.
- `-o <plik>` – pobiera plik i zapisuje go pod określoną nazwą.
- `-I` – pobiera tylko nagłówki odpowiedzi.
- `-L` – podąża za przekierowaniami.
- `-d <dane>` – wysyła dane w żądaniu POST.
- `-H <nagłówek>` – dodaje nagłówek do żądania.

## Common Examples
Oto kilka praktycznych przykładów użycia `curl`:

1. **Pobieranie pliku z internetu:**
   ```bash
   curl -O https://example.com/plik.txt
   ```

2. **Pobieranie pliku i zapisywanie go pod inną nazwą:**
   ```bash
   curl -o nowy_plik.txt https://example.com/plik.txt
   ```

3. **Pobieranie tylko nagłówków odpowiedzi:**
   ```bash
   curl -I https://example.com
   ```

4. **Wysyłanie danych w żądaniu POST:**
   ```bash
   curl -d "parametr1=wartosc1&parametr2=wartosc2" https://example.com/api
   ```

5. **Podążanie za przekierowaniami:**
   ```bash
   curl -L https://example.com
   ```

## Tips
- Używaj opcji `-O`, aby łatwo pobierać pliki z ich oryginalnymi nazwami.
- Zawsze sprawdzaj nagłówki odpowiedzi, aby upewnić się, że żądanie zakończyło się sukcesem.
- Jeśli pracujesz z API, pamiętaj o dodawaniu odpowiednich nagłówków, aby autoryzować swoje żądania.
- Możesz używać `-v` (verbose), aby uzyskać więcej informacji o przebiegu żądania, co jest przydatne w przypadku debugowania.