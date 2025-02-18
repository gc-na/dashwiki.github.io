# [Debian] Debian Almquist Shell (dash) head <Użycie: wyświetlanie pierwszych linii pliku>

## Przegląd
Polecenie `head` w systemie Debian Almquist Shell (dash) służy do wyświetlania pierwszych kilku linii pliku tekstowego. Domyślnie pokazuje pierwsze 10 linii, co jest przydatne do szybkiego podglądu zawartości pliku.

## Użycie
Podstawowa składnia polecenia `head` jest następująca:

```
head [opcje] [argumenty]
```

## Często używane opcje
- `-n NUM` – wyświetla pierwsze NUM linii pliku.
- `-c NUM` – wyświetla pierwsze NUM bajtów pliku.
- `-q` – nie wyświetla nagłówków plików, gdy podano wiele plików.
- `-v` – zawsze wyświetla nagłówki plików, nawet przy jednym pliku.

## Przykłady
Oto kilka praktycznych przykładów użycia polecenia `head`:

1. Wyświetlenie pierwszych 10 linii pliku `plik.txt`:
   ```sh
   head plik.txt
   ```

2. Wyświetlenie pierwszych 5 linii pliku `plik.txt`:
   ```sh
   head -n 5 plik.txt
   ```

3. Wyświetlenie pierwszych 20 bajtów pliku `plik.txt`:
   ```sh
   head -c 20 plik.txt
   ```

4. Wyświetlenie pierwszych 10 linii z wielu plików:
   ```sh
   head plik1.txt plik2.txt
   ```

5. Wyświetlenie nagłówków plików przy wyświetlaniu z wielu plików:
   ```sh
   head -v plik1.txt plik2.txt
   ```

## Wskazówki
- Używaj opcji `-n` dla większej elastyczności w określaniu liczby linii do wyświetlenia.
- Możesz łączyć `head` z innymi poleceniami, takimi jak `grep`, aby filtrować wyniki.
- Przy pracy z dużymi plikami, `head` jest szybszym sposobem na uzyskanie podglądu ich zawartości niż otwieranie całego pliku w edytorze.