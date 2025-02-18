# [Polski] Debian Almquist Shell (dash) cp <Użycie: kopiowanie plików i katalogów>

## Przegląd
Polecenie `cp` służy do kopiowania plików i katalogów w systemie Linux. Umożliwia tworzenie kopii zapasowych oraz przenoszenie danych w obrębie systemu plików.

## Użycie
Podstawowa składnia polecenia `cp` jest następująca:

```bash
cp [opcje] [argumenty]
```

## Częste opcje
- `-r` lub `--recursive`: Kopiuje katalogi rekurencyjnie.
- `-i` lub `--interactive`: Pyta o potwierdzenie przed nadpisaniem istniejącego pliku.
- `-u` lub `--update`: Kopiuje tylko wtedy, gdy źródłowy plik jest nowszy od docelowego lub gdy plik docelowy nie istnieje.
- `-v` lub `--verbose`: Wyświetla szczegóły dotyczące kopiowanych plików.

## Częste przykłady
1. Kopiowanie pliku do innej lokalizacji:

   ```bash
   cp plik.txt /ścieżka/do/docelowego/
   ```

2. Kopiowanie katalogu rekurencyjnie:

   ```bash
   cp -r katalog/ /ścieżka/do/docelowego/
   ```

3. Kopiowanie z potwierdzeniem przed nadpisaniem:

   ```bash
   cp -i plik.txt /ścieżka/do/docelowego/
   ```

4. Kopiowanie tylko nowszych plików:

   ```bash
   cp -u plik.txt /ścieżka/do/docelowego/
   ```

5. Wyświetlanie szczegółów podczas kopiowania:

   ```bash
   cp -v plik.txt /ścieżka/do/docelowego/
   ```

## Wskazówki
- Zawsze używaj opcji `-i`, gdy kopiujesz pliki do lokalizacji, gdzie mogą istnieć pliki o tej samej nazwie, aby uniknąć przypadkowego nadpisania.
- Używaj opcji `-r` z rozwagą, aby nie skopiować niezamierzonych plików lub katalogów.
- Regularnie twórz kopie zapasowe ważnych plików, aby zabezpieczyć się przed ich utratą.