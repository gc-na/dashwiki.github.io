# [Debian] Debian Almquist Shell (dash) diff: porównywanie plików

## Overview
Polecenie `diff` służy do porównywania zawartości dwóch plików tekstowych. Umożliwia użytkownikowi zobaczenie różnic między tymi plikami, co jest szczególnie przydatne w programowaniu, edytowaniu dokumentów oraz w zarządzaniu wersjami.

## Usage
Podstawowa składnia polecenia `diff` jest następująca:

```bash
diff [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `diff`:

- `-u`: Wyświetla różnice w formacie z jedną kontekstem (unified).
- `-c`: Wyświetla różnice w formacie kontekstowym.
- `-i`: Ignoruje różnice w wielkości liter.
- `-w`: Ignoruje różnice w białych znakach.
- `-r`: Porównuje katalogi rekurencyjnie.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `diff`:

1. Porównanie dwóch plików tekstowych:
   ```bash
   diff plik1.txt plik2.txt
   ```

2. Porównanie dwóch plików z uwzględnieniem wielkości liter:
   ```bash
   diff -i plik1.txt plik2.txt
   ```

3. Porównanie dwóch katalogów rekurencyjnie:
   ```bash
   diff -r katalog1/ katalog2/
   ```

4. Wyświetlenie różnic w formacie z jedną kontekstem:
   ```bash
   diff -u plik1.txt plik2.txt
   ```

## Tips
- Używaj opcji `-u`, aby uzyskać bardziej czytelne różnice, które są łatwiejsze do zrozumienia.
- Jeśli często porównujesz te same pliki, rozważ stworzenie skryptu, który automatyzuje to zadanie.
- Zapisz wyniki polecenia `diff` do pliku, używając przekierowania, aby mieć je na później:
  ```bash
  diff plik1.txt plik2.txt > różnice.txt
  ```