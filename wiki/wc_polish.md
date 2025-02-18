# [Polski] Debian Almquist Shell (dash) wc użycie: Zliczanie linii, słów i bajtów

## Overview
Polecenie `wc` (word count) służy do zliczania linii, słów i bajtów w plikach tekstowych. Jest to przydatne narzędzie do szybkiej analizy zawartości plików.

## Usage
Podstawowa składnia polecenia `wc` jest następująca:

```bash
wc [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `wc`:

- `-l`: Zlicza tylko linie.
- `-w`: Zlicza tylko słowa.
- `-c`: Zlicza tylko bajty.
- `-m`: Zlicza tylko znaki (w tym przypadku uwzględnia znaki multibyte).
- `-L`: Zwraca długość najdłuższej linii.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `wc`:

1. Zliczanie wszystkich linii, słów i bajtów w pliku:

   ```bash
   wc plik.txt
   ```

2. Zliczanie tylko linii w pliku:

   ```bash
   wc -l plik.txt
   ```

3. Zliczanie tylko słów w pliku:

   ```bash
   wc -w plik.txt
   ```

4. Zliczanie tylko bajtów w pliku:

   ```bash
   wc -c plik.txt
   ```

5. Zliczanie długości najdłuższej linii w pliku:

   ```bash
   wc -L plik.txt
   ```

## Tips
- Używaj opcji `-l`, `-w` i `-c` razem, aby uzyskać pełny raport o pliku w jednym poleceniu.
- Możesz używać `wc` w połączeniu z innymi poleceniami, na przykład z `cat`, aby zliczyć zawartość wielu plików:
  
  ```bash
  cat plik1.txt plik2.txt | wc
  ```

- Pamiętaj, że `wc` może również działać na danych wejściowych z potoku, co czyni go bardzo elastycznym narzędziem.