# [Polski] Debian Almquist Shell (dash) netcat użycie: Narzędzie do komunikacji sieciowej

## Overview
Netcat, znany również jako "nc", to wszechstronne narzędzie do komunikacji sieciowej, które umożliwia przesyłanie danych przez protokoły TCP i UDP. Jest często używane do debugowania i testowania połączeń sieciowych, a także jako prosty serwer lub klient.

## Usage
Podstawowa składnia polecenia netcat wygląda następująco:

```bash
netcat [opcje] [argumenty]
```

## Common Options
- `-l`: Uruchamia netcat w trybie nasłuchującym (serwer).
- `-p [port]`: Ustala port, na którym netcat będzie nasłuchiwać lub łączyć się.
- `-u`: Używa protokołu UDP zamiast TCP.
- `-v`: Włącza tryb szczegółowy, wyświetlając więcej informacji o połączeniu.
- `-z`: Używa trybu skanowania, nie przesyłając danych, tylko sprawdzając dostępność portów.

## Common Examples
1. **Nasłuchiwanie na porcie 1234:**
   ```bash
   netcat -l -p 1234
   ```

2. **Łączenie się z serwerem na porcie 80:**
   ```bash
   netcat example.com 80
   ```

3. **Wysyłanie pliku przez netcat:**
   ```bash
   netcat -l -p 1234 > received_file.txt
   ```
   W innym terminalu:
   ```bash
   netcat localhost 1234 < file_to_send.txt
   ```

4. **Skanowanie portów na hoście:**
   ```bash
   netcat -zv example.com 1-1000
   ```

## Tips
- Używaj opcji `-v`, aby uzyskać więcej informacji podczas nawiązywania połączeń.
- Pamiętaj, że netcat nie szyfruje danych, więc unikaj przesyłania poufnych informacji.
- Możesz używać netcat do tworzenia prostych tuneli TCP, co może być przydatne w różnych scenariuszach sieciowych.