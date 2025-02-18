# [Debian] Debian Almquist Shell (dash) find użycie: znajdowanie nazw plików

## Overview
Polecenie `find` służy do przeszukiwania systemu plików w poszukiwaniu plików i katalogów, które spełniają określone kryteria. Umożliwia użytkownikom lokalizowanie plików na podstawie różnych atrybutów, takich jak nazwa, typ, rozmiar czy data modyfikacji.

## Usage
Podstawowa składnia polecenia `find` jest następująca:

```
find [ścieżka] [opcje] [argumenty]
```

## Common Options
Oto niektóre z najczęściej używanych opcji polecenia `find`:

- `-name [nazwa]`: wyszukuje pliki o podanej nazwie.
- `-type [typ]`: filtruje wyniki według typu pliku (np. `f` dla plików, `d` dla katalogów).
- `-size [rozmiar]`: wyszukuje pliki o określonym rozmiarze.
- `-mtime [liczba]`: znajduje pliki zmodyfikowane w ciągu ostatnich `liczba` dni.
- `-exec [polecenie] {} \;`: wykonuje polecenie na każdym znalezionym pliku.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `find`:

1. Znajdowanie plików o nazwie `example.txt` w bieżącym katalogu i podkatalogach:
   ```bash
   find . -name "example.txt"
   ```

2. Wyszukiwanie wszystkich katalogów w systemie:
   ```bash
   find / -type d
   ```

3. Znajdowanie plików większych niż 10 MB:
   ```bash
   find . -type f -size +10M
   ```

4. Wyszukiwanie plików zmodyfikowanych w ciągu ostatnich 7 dni:
   ```bash
   find . -mtime -7
   ```

5. Usuwanie plików tymczasowych z katalogu `/tmp`:
   ```bash
   find /tmp -type f -name "*.tmp" -exec rm {} \;
   ```

## Tips
- Używaj opcji `-print` na końcu polecenia, aby wyświetlić wyniki, jeśli nie są one domyślnie wyświetlane.
- Zawsze testuj polecenia `find` bez opcji `-exec`, aby upewnić się, że zwracają oczekiwane wyniki, zanim wykonasz jakiekolwiek operacje na plikach.
- Możesz łączyć różne opcje, aby precyzyjniej określić kryteria wyszukiwania, co zwiększy efektywność polecenia.