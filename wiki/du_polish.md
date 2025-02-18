# [Debian] Debian Almquist Shell (dash) du użycie: Sprawdza rozmiar katalogów i plików

## Overview
Polecenie `du` (disk usage) służy do wyświetlania rozmiaru katalogów i plików w systemie plików. Umożliwia użytkownikom zrozumienie, ile miejsca zajmują różne elementy na dysku, co jest przydatne przy zarządzaniu przestrzenią dyskową.

## Usage
Podstawowa składnia polecenia `du` jest następująca:

```bash
du [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `du`:

- `-h`: Wyświetla rozmiary w formacie czytelnym dla ludzi (np. KB, MB).
- `-s`: Podsumowuje rozmiar dla każdego argumentu, zamiast wyświetlać rozmiary dla wszystkich podkatalogów.
- `-a`: Wyświetla rozmiary dla wszystkich plików i katalogów, a nie tylko dla katalogów.
- `-c`: Wyświetla całkowity rozmiar na końcu listy.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `du`:

1. Aby sprawdzić rozmiar bieżącego katalogu i jego podkatalogów:
   ```bash
   du
   ```

2. Aby uzyskać czytelny dla ludzi rozmiar katalogu:
   ```bash
   du -h
   ```

3. Aby uzyskać podsumowanie rozmiaru dla konkretnego katalogu:
   ```bash
   du -sh /ścieżka/do/katalogu
   ```

4. Aby wyświetlić rozmiary wszystkich plików i katalogów w bieżącym katalogu:
   ```bash
   du -ah
   ```

5. Aby uzyskać całkowity rozmiar wszystkich plików i katalogów:
   ```bash
   du -ch
   ```

## Tips
- Używaj opcji `-h`, aby łatwiej interpretować rozmiary, zwłaszcza w dużych katalogach.
- Opcja `-s` jest przydatna, gdy chcesz szybko sprawdzić rozmiar konkretnego katalogu bez przeszukiwania wszystkich podkatalogów.
- Regularne monitorowanie rozmiarów katalogów może pomóc w zarządzaniu przestrzenią dyskową i unikaniu problemów z brakiem miejsca.