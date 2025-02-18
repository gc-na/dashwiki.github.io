# [Debian] Debian Almquist Shell (dash) bzip2 Użycie: kompresja plików

## Przegląd
Polecenie `bzip2` służy do kompresji plików, zmniejszając ich rozmiar, co ułatwia przechowywanie i przesyłanie. Używa algorytmu Burrows-Wheeler, który zapewnia wysoką efektywność kompresji.

## Użycie
Podstawowa składnia polecenia `bzip2` jest następująca:

```bash
bzip2 [opcje] [argumenty]
```

## Często używane opcje
- `-d`, `--decompress`: dekompresuje plik.
- `-k`, `--keep`: zachowuje oryginalny plik po kompresji.
- `-f`, `--force`: wymusza nadpisanie istniejących plików.
- `-v`, `--verbose`: wyświetla szczegółowe informacje o procesie kompresji.

## Przykłady
Oto kilka praktycznych przykładów użycia polecenia `bzip2`:

1. Kompresja pliku:
   ```bash
   bzip2 plik.txt
   ```

2. Dekompresja pliku:
   ```bash
   bzip2 -d plik.txt.bz2
   ```

3. Kompresja pliku z zachowaniem oryginału:
   ```bash
   bzip2 -k plik.txt
   ```

4. Wymuszenie nadpisania istniejącego pliku:
   ```bash
   bzip2 -f plik.txt
   ```

5. Wyświetlenie szczegółowych informacji podczas kompresji:
   ```bash
   bzip2 -v plik.txt
   ```

## Wskazówki
- Zawsze sprawdzaj, czy masz kopię zapasową ważnych plików przed ich kompresją.
- Używaj opcji `-k`, jeśli chcesz zachować oryginalne pliki, co jest przydatne w przypadku testowania kompresji.
- Pamiętaj, że pliki skompresowane za pomocą `bzip2` mają rozszerzenie `.bz2`, co ułatwia ich identyfikację.