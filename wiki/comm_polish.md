# [Polski] Debian Almquist Shell (dash) comm: porównywanie plików tekstowych

## Overview
Polecenie `comm` służy do porównywania dwóch posortowanych plików tekstowych linia po linii. Umożliwia wyświetlenie linii, które są wspólne dla obu plików, linii, które występują tylko w pierwszym pliku oraz linii, które występują tylko w drugim pliku.

## Usage
Podstawowa składnia polecenia `comm` jest następująca:

```bash
comm [opcje] [plik1] [plik2]
```

## Common Options
- `-1`: Ukrywa linie, które występują tylko w pierwszym pliku.
- `-2`: Ukrywa linie, które występują tylko w drugim pliku.
- `-3`: Ukrywa linie, które są wspólne dla obu plików.
- `-i`: Ignoruje różnice w wielkości liter podczas porównywania.
- `-u`: Wyświetla unikalne linie z obu plików.

## Common Examples
1. Porównanie dwóch plików i wyświetlenie wszystkich linii:
   ```bash
   comm plik1.txt plik2.txt
   ```

2. Wyświetlenie tylko linii, które występują w pierwszym pliku:
   ```bash
   comm -13 plik1.txt plik2.txt
   ```

3. Wyświetlenie tylko linii, które występują w drugim pliku:
   ```bash
   comm -12 plik1.txt plik2.txt
   ```

4. Porównanie plików bez uwzględniania wielkości liter:
   ```bash
   comm -i plik1.txt plik2.txt
   ```

5. Wyświetlenie unikalnych linii z obu plików:
   ```bash
   comm -u plik1.txt plik2.txt
   ```

## Tips
- Upewnij się, że pliki są posortowane przed użyciem `comm`, ponieważ polecenie działa poprawnie tylko na posortowanych danych.
- Możesz użyć `sort` w połączeniu z `comm`, aby automatycznie posortować pliki:
  ```bash
  comm <(sort plik1.txt) <(sort plik2.txt)
  ```
- W przypadku dużych plików, rozważ użycie opcji `-1`, `-2` lub `-3`, aby skupić się tylko na interesujących cię liniach.