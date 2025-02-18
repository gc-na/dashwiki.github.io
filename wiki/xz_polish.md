# [Debian] Debian Almquist Shell (dash) xz: Kompresja i dekompresja plików

## Przegląd
Polecenie `xz` służy do kompresji i dekompresji plików przy użyciu algorytmu LZMA. Jest to narzędzie, które pozwala na znaczne zmniejszenie rozmiaru plików, co jest przydatne w celu oszczędzania miejsca na dysku oraz szybszego przesyłania danych.

## Użycie
Podstawowa składnia polecenia `xz` jest następująca:

```bash
xz [opcje] [argumenty]
```

## Częste opcje
- `-d`, `--decompress`: dekompresuje plik.
- `-k`, `--keep`: zachowuje oryginalny plik po kompresji.
- `-f`, `--force`: wymusza kompresję, nawet jeśli plik już istnieje.
- `-z`, `--compress`: kompresuje plik (domyślna opcja).
- `-9`: ustawia maksymalny poziom kompresji.

## Przykłady
1. Kompresja pliku:
   ```bash
   xz myfile.txt
   ```
   To polecenie skompresuje plik `myfile.txt`, tworząc plik `myfile.txt.xz`.

2. Dekomprensja pliku:
   ```bash
   xz -d myfile.txt.xz
   ```
   To polecenie przywróci oryginalny plik `myfile.txt` z pliku skompresowanego `myfile.txt.xz`.

3. Kompresja z zachowaniem oryginału:
   ```bash
   xz -k myfile.txt
   ```
   Plik `myfile.txt` zostanie skompresowany, a oryginał pozostanie nietknięty.

4. Wymuszenie kompresji:
   ```bash
   xz -f myfile.txt
   ```
   To polecenie wymusi kompresję pliku, nawet jeśli plik `myfile.txt.xz` już istnieje.

## Wskazówki
- Używaj opcji `-k`, jeśli chcesz zachować oryginalne pliki po kompresji.
- Zawsze sprawdzaj rozmiar pliku po kompresji, aby upewnić się, że osiągnąłeś oczekiwany poziom kompresji.
- Eksperymentuj z różnymi poziomami kompresji (np. `-1` do `-9`), aby znaleźć najlepszy balans między czasem kompresji a rozmiarem pliku.