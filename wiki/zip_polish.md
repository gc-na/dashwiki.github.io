# [Polski] Debian Almquist Shell (dash) zip użycie: kompresja plików

## Overview
Polecenie `zip` służy do kompresji plików i tworzenia archiwów w formacie ZIP. Umożliwia łatwe pakowanie wielu plików w jeden plik, co ułatwia ich przechowywanie i przesyłanie.

## Usage
Podstawowa składnia polecenia `zip` jest następująca:

```bash
zip [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji polecenia `zip`:

- `-r`: Rekurencyjnie dodaje pliki i katalogi.
- `-e`: Szyfruje archiwum hasłem.
- `-u`: Aktualizuje istniejące pliki w archiwum.
- `-d`: Usuwa pliki z archiwum.
- `-l`: Wyświetla listę plików w archiwum.

## Common Examples
Poniżej znajdują się przykłady użycia polecenia `zip`:

1. Tworzenie archiwum ZIP z pojedynczego pliku:
   ```bash
   zip archiwum.zip plik.txt
   ```

2. Tworzenie archiwum ZIP z wielu plików:
   ```bash
   zip archiwum.zip plik1.txt plik2.txt plik3.txt
   ```

3. Rekurencyjne dodawanie wszystkich plików z katalogu:
   ```bash
   zip -r archiwum.zip katalog/
   ```

4. Szyfrowanie archiwum hasłem:
   ```bash
   zip -e archiwum.zip plik.txt
   ```

5. Aktualizacja plików w istniejącym archiwum:
   ```bash
   zip -u archiwum.zip plik2.txt
   ```

## Tips
- Używaj opcji `-r`, gdy chcesz skompresować cały katalog, aby nie pominąć żadnych plików.
- Pamiętaj, aby nie używać zbyt prostych haseł, gdy szyfrujesz archiwum, aby zwiększyć bezpieczeństwo.
- Regularnie aktualizuj swoje archiwa, aby mieć pewność, że zawierają najnowsze wersje plików.