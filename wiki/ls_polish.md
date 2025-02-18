# [Debian] Debian Almquist Shell (dash) ls użycie: Wyświetlanie zawartości katalogu

## Przegląd
Polecenie `ls` służy do wyświetlania listy plików i katalogów w danym katalogu. Jest to jedno z najczęściej używanych poleceń w systemach Unix i Linux, umożliwiające użytkownikom szybki przegląd zawartości folderów.

## Użycie
Podstawowa składnia polecenia `ls` jest następująca:

```
ls [opcje] [argumenty]
```

## Częste opcje
- `-l` : Wyświetla szczegółowe informacje o plikach i katalogach w formacie długim.
- `-a` : Wyświetla wszystkie pliki, w tym ukryte (zaczynające się od kropki).
- `-h` : Wyświetla rozmiary plików w formacie czytelnym dla ludzi (np. KB, MB).
- `-R` : Rekursywnie wyświetla zawartość katalogów.
- `-t` : Sortuje pliki według daty modyfikacji, od najnowszych do najstarszych.

## Częste przykłady
1. Wyświetlenie zawartości bieżącego katalogu:
   ```bash
   ls
   ```

2. Wyświetlenie szczegółowych informacji o plikach:
   ```bash
   ls -l
   ```

3. Wyświetlenie wszystkich plików, w tym ukrytych:
   ```bash
   ls -a
   ```

4. Wyświetlenie rozmiarów plików w formacie czytelnym:
   ```bash
   ls -lh
   ```

5. Rekursywne wyświetlenie zawartości katalogów:
   ```bash
   ls -R
   ```

6. Sortowanie plików według daty modyfikacji:
   ```bash
   ls -lt
   ```

## Wskazówki
- Używaj opcji `-h` w połączeniu z `-l`, aby uzyskać bardziej czytelne informacje o rozmiarach plików.
- Możesz łączyć różne opcje, na przykład `ls -la` wyświetli wszystkie pliki w formacie długim.
- Jeśli chcesz wyświetlić zawartość innego katalogu, wystarczy podać jego ścieżkę jako argument, np. `ls /ścieżka/do/katalogu`.