# [Debian] Debian Almquist Shell (dash) awk użycie: Przetwarzanie tekstu

## Overview
Polecenie `awk` jest potężnym narzędziem do przetwarzania tekstu, które pozwala na analizowanie i manipulowanie danymi w formacie tekstowym. Umożliwia wykonywanie operacji na wierszach i kolumnach danych, co czyni go niezwykle przydatnym w skryptach i analizach.

## Usage
Podstawowa składnia polecenia `awk` jest następująca:

```bash
awk [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla `awk`:

- `-F` - Ustawia separator pól (domyślnie jest to spacja).
- `-v` - Umożliwia przekazywanie zmiennych do skryptu `awk`.
- `-f` - Umożliwia załadowanie skryptu `awk` z pliku.
- `-W` - Umożliwia włączenie dodatkowych funkcji, takich jak `compat` dla zgodności z innymi wersjami `awk`.

## Common Examples
Oto kilka praktycznych przykładów użycia `awk`:

1. **Wyświetlanie drugiej kolumny z pliku:**

   ```bash
   awk '{print $2}' plik.txt
   ```

2. **Zliczanie liczby wierszy w pliku:**

   ```bash
   awk 'END {print NR}' plik.txt
   ```

3. **Filtracja wierszy zawierających określony tekst:**

   ```bash
   awk '/szukany_tekst/' plik.txt
   ```

4. **Zmiana separatora na przecinek i wyświetlanie pierwszej kolumny:**

   ```bash
   awk -F, '{print $1}' plik.csv
   ```

5. **Obliczanie sumy wartości w trzeciej kolumnie:**

   ```bash
   awk '{sum += $3} END {print sum}' plik.txt
   ```

## Tips
- Używaj opcji `-F` do ustawienia separatora, aby dostosować `awk` do różnych formatów plików.
- Możesz łączyć `awk` z innymi poleceniami, używając potoku (`|`), aby tworzyć bardziej złożone skrypty.
- Zawsze testuj swoje skrypty na małych próbkach danych, aby upewnić się, że działają zgodnie z oczekiwaniami przed zastosowaniem ich na większych zbiorach danych.