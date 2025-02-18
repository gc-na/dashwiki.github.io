# [Polski] Debian Almquist Shell (dash) basename użycie: Usuwa ścieżki i rozszerzenia plików

## Przegląd
Polecenie `basename` służy do usuwania ścieżek i rozszerzeń z nazw plików. Umożliwia to uzyskanie samej nazwy pliku, co jest przydatne w skryptach i operacjach na plikach.

## Użycie
Podstawowa składnia polecenia `basename` jest następująca:

```bash
basename [opcje] [argumenty]
```

## Typowe opcje
- `-a`: Obsługuje wiele argumentów, zwracając nazwy plików dla każdego z nich.
- `-s`: Usuwa określone rozszerzenie z nazwy pliku.
  
## Typowe przykłady
Oto kilka praktycznych przykładów użycia polecenia `basename`:

1. Uzyskanie samej nazwy pliku z pełnej ścieżki:
   ```bash
   basename /usr/local/bin/skrypt.sh
   ```
   Wynik: `skrypt.sh`

2. Usunięcie rozszerzenia z nazwy pliku:
   ```bash
   basename /usr/local/bin/skrypt.sh .sh
   ```
   Wynik: `skrypt`

3. Obsługa wielu plików:
   ```bash
   basename -a /usr/local/bin/skrypt1.sh /usr/local/bin/skrypt2.sh
   ```
   Wynik:
   ```
   skrypt1.sh
   skrypt2.sh
   ```

4. Usunięcie niestandardowego rozszerzenia:
   ```bash
   basename /path/to/file.txt .txt
   ```
   Wynik: `file`

## Wskazówki
- Używaj opcji `-a`, gdy chcesz przetwarzać wiele plików jednocześnie.
- Zawsze podawaj pełną ścieżkę, aby uniknąć nieporozumień z nazwami plików w bieżącym katalogu.
- Możesz łączyć `basename` z innymi poleceniami w skryptach, aby dynamicznie przetwarzać nazwy plików.