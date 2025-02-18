# [Debian] Debian Almquist Shell (dash) cmp użycie: Porównywanie plików

## Overview
Polecenie `cmp` służy do porównywania dwóch plików binarnych lub tekstowych w celu określenia, czy są one identyczne. Jeśli pliki różnią się, `cmp` wskaże pierwszą różnicę, co pozwala na łatwe zidentyfikowanie miejsc, w których pliki się różnią.

## Usage
Podstawowa składnia polecenia `cmp` jest następująca:

```
cmp [opcje] [argumenty]
```

## Common Options
- `-l` – Wyświetla numery bajtów, w których pliki różnią się, oraz wartości tych bajtów w systemie ósemkowym.
- `-s` – Porównuje pliki w trybie cichym; nie wyświetla żadnych komunikatów, tylko zwraca kod wyjścia.
- `-i OFFSET` – Pomija pierwsze `OFFSET` bajtów w obu plikach przed porównywaniem.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `cmp`:

1. Porównanie dwóch plików:
   ```bash
   cmp plik1.txt plik2.txt
   ```

2. Porównanie dwóch plików w trybie cichym:
   ```bash
   cmp -s plik1.bin plik2.bin
   ```

3. Wyświetlenie różnic w formie numerycznej:
   ```bash
   cmp -l plik1.txt plik2.txt
   ```

4. Pominięcie pierwszych 10 bajtów podczas porównywania:
   ```bash
   cmp -i 10 plik1.bin plik2.bin
   ```

## Tips
- Używaj opcji `-s`, gdy chcesz szybko sprawdzić, czy pliki są identyczne, bez zbędnych informacji.
- Opcja `-l` jest przydatna, gdy potrzebujesz szczegółowych informacji o różnicach między plikami.
- Pamiętaj, że `cmp` porównuje pliki bajt po bajcie, więc nawet drobne różnice, takie jak spacje czy nowe linie, będą wykrywane.