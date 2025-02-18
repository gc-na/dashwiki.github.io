# [Debian] Debian Almquist Shell (dash) mv Użycie: Przenoszenie i zmiana nazw plików

## Overview
Polecenie `mv` w systemie Debian Almquist Shell (dash) służy do przenoszenia plików i katalogów oraz zmiany ich nazw. Jest to podstawowe narzędzie do zarządzania plikami w systemie operacyjnym Linux.

## Usage
Podstawowa składnia polecenia `mv` wygląda następująco:

```
mv [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `mv`:

- `-i`: Pyta o potwierdzenie przed nadpisaniem istniejącego pliku.
- `-u`: Przenosi plik tylko wtedy, gdy źródło jest nowsze niż cel lub gdy cel nie istnieje.
- `-v`: Wyświetla szczegóły operacji przenoszenia.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `mv`:

1. **Przenoszenie pliku do innego katalogu:**
   ```bash
   mv dokument.txt /home/użytkownik/dokumenty/
   ```

2. **Zmiana nazwy pliku:**
   ```bash
   mv stary_nazwa.txt nowy_nazwa.txt
   ```

3. **Przenoszenie wielu plików do katalogu:**
   ```bash
   mv plik1.txt plik2.txt /home/użytkownik/dokumenty/
   ```

4. **Przenoszenie pliku z potwierdzeniem przed nadpisaniem:**
   ```bash
   mv -i dokument.txt /home/użytkownik/dokumenty/
   ```

5. **Przenoszenie pliku tylko jeśli jest nowszy:**
   ```bash
   mv -u dokument.txt /home/użytkownik/dokumenty/
   ```

## Tips
- Zawsze używaj opcji `-i`, gdy przenosisz pliki, które mogą nadpisać istniejące pliki, aby uniknąć przypadkowej utraty danych.
- Używaj opcji `-v`, aby mieć lepszy wgląd w to, co się dzieje podczas przenoszenia plików.
- Przy przenoszeniu wielu plików, upewnij się, że cel jest katalogiem, aby uniknąć błędów.