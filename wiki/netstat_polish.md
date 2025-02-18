# [Debian] Debian Almquist Shell (dash) netstat użycie: wyświetlanie informacji o połączeniach sieciowych

## Overview
Polecenie `netstat` służy do wyświetlania informacji o połączeniach sieciowych, tabel routingu, statystykach interfejsów oraz innych danych związanych z siecią. Jest to przydatne narzędzie do monitorowania aktywności sieciowej i diagnozowania problemów.

## Usage
Podstawowa składnia polecenia `netstat` jest następująca:

```bash
netstat [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `netstat`:

- `-a`: Wyświetla wszystkie połączenia i porty nasłuchujące.
- `-t`: Pokazuje tylko połączenia TCP.
- `-u`: Pokazuje tylko połączenia UDP.
- `-n`: Wyświetla adresy i numery portów w formacie numerycznym, zamiast próbować rozwiązywać je na nazwy.
- `-l`: Wyświetla tylko porty nasłuchujące.
- `-p`: Pokazuje identyfikatory procesów (PID) oraz nazwy programów, które używają portów.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `netstat`:

1. Wyświetlenie wszystkich aktywnych połączeń i portów nasłuchujących:

   ```bash
   netstat -a
   ```

2. Wyświetlenie tylko połączeń TCP:

   ```bash
   netstat -t
   ```

3. Wyświetlenie portów nasłuchujących:

   ```bash
   netstat -l
   ```

4. Wyświetlenie połączeń z numerami portów w formacie numerycznym:

   ```bash
   netstat -n
   ```

5. Wyświetlenie połączeń z informacjami o procesach:

   ```bash
   netstat -p
   ```

## Tips
- Używaj opcji `-n`, aby przyspieszyć wyświetlanie wyników, zwłaszcza w dużych sieciach.
- Łącz różne opcje, aby uzyskać bardziej szczegółowe informacje, na przykład `netstat -tuln` wyświetli wszystkie porty TCP i UDP w formacie numerycznym.
- Regularnie monitoruj połączenia sieciowe, aby szybko wykrywać nieautoryzowane połączenia lub problemy z siecią.