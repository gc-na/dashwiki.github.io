# [Polski] Debian Almquist Shell (dash) unxz użycie: Rozpakowywanie plików .xz

## Przegląd
Polecenie `unxz` służy do dekompresji plików skompresowanych przy użyciu algorytmu XZ. Jest to prosty sposób na przywrócenie oryginalnych plików z formatu .xz.

## Użycie
Podstawowa składnia polecenia `unxz` jest następująca:

```
unxz [opcje] [argumenty]
```

## Częste opcje
- `-k`, `--keep`: Zachowuje oryginalny plik skompresowany po dekompresji.
- `-f`, `--force`: Wymusza dekompresję, nawet jeśli plik docelowy już istnieje.
- `-v`, `--verbose`: Wyświetla szczegółowe informacje o postępie dekompresji.

## Przykłady
Oto kilka praktycznych przykładów użycia polecenia `unxz`:

1. Aby rozpakować plik `example.xz`:
   ```bash
   unxz example.xz
   ```

2. Aby rozpakować plik i zachować oryginalny plik .xz:
   ```bash
   unxz -k example.xz
   ```

3. Aby wymusić dekompresję pliku, nawet jeśli plik docelowy już istnieje:
   ```bash
   unxz -f example.xz
   ```

4. Aby uzyskać szczegółowe informacje podczas dekompresji:
   ```bash
   unxz -v example.xz
   ```

## Wskazówki
- Używaj opcji `-k`, jeśli chcesz zachować skompresowany plik na wypadek, gdyby dekompresja nie powiodła się.
- Zawsze sprawdzaj, czy masz odpowiednie uprawnienia do zapisu w katalogu, w którym dekompresujesz pliki.
- Możesz użyć `unxz` w skryptach, aby automatycznie dekompresować pliki w procesach przetwarzania danych.