# [Polski] Debian Almquist Shell (dash) test użycie: Sprawdzanie warunków

## Overview
Polecenie `test` w powłoce Debian Almquist Shell (dash) służy do oceny warunków i zwracania statusu wyjścia na podstawie tych warunków. Jest często używane w skryptach powłoki do podejmowania decyzji na podstawie różnych kryteriów, takich jak istnienie plików, porównania liczb czy sprawdzanie typów plików.

## Usage
Podstawowa składnia polecenia `test` jest następująca:

```sh
test [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `test`:

- `-e FILE`: Sprawdza, czy plik istnieje.
- `-f FILE`: Sprawdza, czy plik jest zwykłym plikiem.
- `-d FILE`: Sprawdza, czy plik jest katalogiem.
- `-z STRING`: Sprawdza, czy długość ciągu jest równa zeru.
- `-n STRING`: Sprawdza, czy długość ciągu jest większa od zera.
- `NUM1 -eq NUM2`: Sprawdza, czy dwie liczby są równe.
- `NUM1 -lt NUM2`: Sprawdza, czy NUM1 jest mniejsze od NUM2.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `test`:

### Sprawdzanie istnienia pliku
```sh
test -e /path/to/file && echo "Plik istnieje."
```

### Sprawdzanie, czy plik jest katalogiem
```sh
test -d /path/to/directory && echo "To jest katalog."
```

### Sprawdzanie długości ciągu
```sh
my_string="Hello"
test -n "$my_string" && echo "Ciąg nie jest pusty."
```

### Porównanie dwóch liczb
```sh
num1=5
num2=10
test $num1 -lt $num2 && echo "$num1 jest mniejsze od $num2."
```

## Tips
- Używaj `[` jako skrótu dla `test`, co może poprawić czytelność skryptów:
  ```sh
  [ -e /path/to/file ] && echo "Plik istnieje."
  ```
- Zawsze pamiętaj o używaniu cudzysłowów wokół zmiennych, aby uniknąć błędów w przypadku pustych lub zawierających spacje wartości.
- Możesz łączyć wiele warunków za pomocą operatorów logicznych `&&` (i) oraz `||` (lub) dla bardziej złożonych sprawdzeń.