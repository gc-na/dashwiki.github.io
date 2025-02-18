# [Debian] Debian Almquist Shell (dash) getopts użycie: [parsowanie opcji skryptów]

## Overview
Polecenie `getopts` w powłoce Debian Almquist Shell (dash) służy do przetwarzania opcji w skryptach powłoki. Umożliwia łatwe analizowanie argumentów przekazywanych do skryptu, co pozwala na obsługę opcji w formacie `-o` lub `--option`.

## Usage
Podstawowa składnia polecenia `getopts` jest następująca:

```sh
getopts optstring variable
```

Gdzie `optstring` to ciąg znaków definiujący dostępne opcje, a `variable` to zmienna, w której będą przechowywane przetwarzane opcje.

## Common Options
- `-o`: Definiuje opcje, które mogą być używane w skrypcie.
- `-a`: Umożliwia przetwarzanie opcji z długimi nazwami (np. `--option`).
- `-n`: Umożliwia określenie nazwy programu, która będzie wyświetlana w komunikatach o błędach.

## Common Examples

### Przykład 1: Prosty skrypt z jedną opcją
```sh
#!/bin/dash

while getopts "f:" opt; do
  case $opt in
    f)
      echo "Plik: $OPTARG"
      ;;
    *)
      echo "Nieznana opcja"
      ;;
  esac
done
```
W tym przykładzie skrypt przetwarza opcję `-f`, która oczekuje argumentu.

### Przykład 2: Obsługa wielu opcji
```sh
#!/bin/dash

while getopts "ab:c" opt; do
  case $opt in
    a)
      echo "Opcja A"
      ;;
    b)
      echo "Opcja B z argumentem: $OPTARG"
      ;;
    c)
      echo "Opcja C"
      ;;
    *)
      echo "Nieznana opcja"
      ;;
  esac
done
```
Tutaj skrypt obsługuje opcje `-a`, `-b` (z argumentem) oraz `-c`.

### Przykład 3: Użycie długich opcji
```sh
#!/bin/dash

while getopts "a:b:c" opt; do
  case $opt in
    a)
      echo "Długa opcja A"
      ;;
    b)
      echo "Długa opcja B z argumentem: $OPTARG"
      ;;
    c)
      echo "Długa opcja C"
      ;;
    *)
      echo "Nieznana opcja"
      ;;
  esac
done
```
W tym przykładzie skrypt może być rozszerzony o długie opcje, ale wymaga dodatkowej logiki do ich obsługi.

## Tips
- Używaj `:` po literze w `optstring`, aby wskazać, że opcja wymaga argumentu.
- Zawsze sprawdzaj zmienną `$OPTIND`, aby upewnić się, że przetwarzanie opcji zakończyło się poprawnie.
- Rozważ użycie `shift` po zakończeniu przetwarzania opcji, aby przejść do pozostałych argumentów skryptu.