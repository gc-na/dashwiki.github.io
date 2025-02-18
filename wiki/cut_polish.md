# [Debian] Debian Almquist Shell (dash) cut użycie: Wyodrębnia dane z plików tekstowych

## Overview
Polecenie `cut` służy do wyodrębniania fragmentów tekstu z plików lub strumieni danych. Umożliwia selekcję określonych kolumn lub znaków, co jest przydatne w przetwarzaniu danych tekstowych.

## Usage
Podstawowa składnia polecenia `cut` wygląda następująco:

```sh
cut [opcje] [argumenty]
```

## Common Options
- `-f` – określa numery pól do wyodrębnienia (oddzielonych separatorem).
- `-d` – definiuje separator, który oddziela pola (domyślnie jest to tabulator).
- `-c` – wybiera konkretne znaki na podstawie ich pozycji.
- `--complement` – zwraca wszystko oprócz wybranych pól lub znaków.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `cut`:

1. Wyodrębnianie drugiego pola z pliku tekstowego, gdzie pola są oddzielone przecinkiem:
   ```sh
   cut -d ',' -f 2 plik.txt
   ```

2. Wyodrębnianie znaków od 1 do 5 z pliku:
   ```sh
   cut -c 1-5 plik.txt
   ```

3. Wyodrębnianie pierwszego i trzeciego pola z pliku, gdzie pola są oddzielone dwukropkiem:
   ```sh
   cut -d ':' -f 1,3 plik.txt
   ```

4. Zwracanie wszystkich pól oprócz drugiego:
   ```sh
   cut -f 2 --complement plik.txt
   ```

## Tips
- Używaj opcji `-n` w przypadku, gdy chcesz uniknąć wyświetlania pustych linii.
- Możesz łączyć `cut` z innymi poleceniami, takimi jak `grep` czy `sort`, aby uzyskać bardziej zaawansowane przetwarzanie danych.
- Zawsze sprawdzaj, czy separator jest poprawnie ustawiony, aby uniknąć nieoczekiwanych wyników.