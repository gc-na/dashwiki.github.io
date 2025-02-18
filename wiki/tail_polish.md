# [Polski] Debian Almquist Shell (dash) tail użycie: Wyświetlanie końcowych linii pliku

## Overview
Polecenie `tail` w systemie Debian Almquist Shell (dash) służy do wyświetlania ostatnich linii pliku. Jest szczególnie przydatne do monitorowania logów lub plików tekstowych, gdzie interesują nas najnowsze wpisy.

## Usage
Podstawowa składnia polecenia `tail` wygląda następująco:

```sh
tail [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `tail`:

- `-n [liczba]`: Wyświetla określoną liczbę ostatnich linii pliku. Na przykład `-n 10` wyświetli ostatnie 10 linii.
- `-f`: Śledzi plik w czasie rzeczywistym, wyświetlając nowe linie, gdy są dodawane. Użyteczne w przypadku logów.
- `-c [liczba]`: Wyświetla określoną liczbę ostatnich bajtów pliku.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `tail`:

1. Wyświetlenie ostatnich 10 linii pliku `log.txt`:
   ```sh
   tail -n 10 log.txt
   ```

2. Śledzenie pliku logów `system.log` w czasie rzeczywistym:
   ```sh
   tail -f system.log
   ```

3. Wyświetlenie ostatnich 50 bajtów pliku `data.txt`:
   ```sh
   tail -c 50 data.txt
   ```

4. Wyświetlenie ostatnich 5 linii pliku `output.txt`:
   ```sh
   tail -n 5 output.txt
   ```

## Tips
- Używaj opcji `-f` w połączeniu z `Ctrl+C`, aby przerwać śledzenie pliku, gdy już nie potrzebujesz jego monitorowania.
- Możesz łączyć `tail` z innymi poleceniami, np. `grep`, aby filtrować wyniki. Na przykład:
  ```sh
  tail -f system.log | grep "error"
  ```
- Pamiętaj, że `tail` działa na plikach tekstowych, więc upewnij się, że plik, który chcesz przeglądać, jest w odpowiednim formacie.