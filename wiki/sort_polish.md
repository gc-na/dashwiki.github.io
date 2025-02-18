# [Debian] Debian Almquist Shell (dash) sort użycie: sortowanie danych

## Overview
Polecenie `sort` w powłoce Debian Almquist Shell (dash) służy do sortowania linii tekstu w plikach lub z wejścia standardowego. Umożliwia uporządkowanie danych w różnych formatach, co jest przydatne w wielu zastosowaniach, takich jak przetwarzanie danych czy analiza tekstu.

## Usage
Podstawowa składnia polecenia `sort` jest następująca:

```bash
sort [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji polecenia `sort`:

- `-n` – sortowanie numeryczne, które traktuje wartości jako liczby.
- `-r` – sortowanie w odwrotnej kolejności (malejąco).
- `-k` – określenie klucza do sortowania, co pozwala na sortowanie według konkretnej kolumny.
- `-u` – usunięcie duplikatów z wyników sortowania.
- `-o` – zapisanie wyników sortowania do określonego pliku.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `sort`:

1. Sortowanie linii w pliku tekstowym:
   ```bash
   sort plik.txt
   ```

2. Sortowanie numeryczne:
   ```bash
   sort -n liczby.txt
   ```

3. Sortowanie w odwrotnej kolejności:
   ```bash
   sort -r plik.txt
   ```

4. Sortowanie według drugiej kolumny:
   ```bash
   sort -k2 plik.txt
   ```

5. Usunięcie duplikatów i zapisanie do nowego pliku:
   ```bash
   sort -u plik.txt -o posortowane.txt
   ```

## Tips
- Używaj opcji `-o`, aby bezpośrednio zapisać posortowane dane do pliku, co może zaoszczędzić czas i zasoby.
- Przy sortowaniu dużych plików, rozważ użycie opcji `-S`, aby określić ilość pamięci, którą `sort` może wykorzystać.
- Zawsze sprawdzaj wyniki sortowania, szczególnie przy użyciu opcji `-u`, aby upewnić się, że nie utraciłeś ważnych danych.