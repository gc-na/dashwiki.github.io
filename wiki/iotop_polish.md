# [Polski] Debian Almquist Shell (dash) iotop użycie: monitorowanie użycia I/O przez procesy

## Przegląd
Polecenie `iotop` służy do monitorowania użycia wejścia/wyjścia (I/O) przez procesy w systemie Linux. Umożliwia użytkownikom obserwację, które procesy generują największy ruch na dysku, co może być pomocne w diagnozowaniu problemów z wydajnością.

## Użycie
Podstawowa składnia polecenia `iotop` jest następująca:

```bash
iotop [opcje] [argumenty]
```

## Typowe opcje
- `-o`, `--only`: Wyświetla tylko procesy, które aktualnie generują I/O.
- `-b`, `--batch`: Uruchamia `iotop` w trybie wsadowym, co jest przydatne do zapisywania wyników do pliku.
- `-n NUM`, `--iterations NUM`: Określa liczbę iteracji, które mają być wykonane przed zakończeniem programu.
- `-d SEC`, `--delay SEC`: Ustala czas opóźnienia między aktualizacjami w sekundach.

## Przykłady
1. Aby uruchomić `iotop` w trybie interaktywnym, wystarczy wpisać:

   ```bash
   iotop
   ```

2. Aby zobaczyć tylko procesy, które aktualnie generują I/O:

   ```bash
   iotop -o
   ```

3. Aby uruchomić `iotop` w trybie wsadowym i zapisać wyniki do pliku:

   ```bash
   iotop -b -n 10 > iotop_output.txt
   ```

4. Aby ustawić opóźnienie między aktualizacjami na 2 sekundy:

   ```bash
   iotop -d 2
   ```

## Wskazówki
- Używaj opcji `-o`, aby szybko zidentyfikować procesy, które powodują największe obciążenie I/O.
- W trybie wsadowym możesz łatwo analizować dane w plikach, co jest przydatne do dalszej analizy.
- Monitoruj I/O w czasie rzeczywistym, aby lepiej zrozumieć, jak różne procesy wpływają na wydajność systemu.