# [Polski] Debian Almquist Shell (dash) dirname Użycie: Uzyskiwanie katalogu z pełnej ścieżki

## Overview
Polecenie `dirname` służy do wyodrębnienia katalogu z pełnej ścieżki pliku. Zwraca część ścieżki, która wskazuje na katalog, w którym znajduje się dany plik.

## Usage
Podstawowa składnia polecenia `dirname` jest następująca:

```bash
dirname [opcje] [argumenty]
```

## Common Options
- `-z`: Zwraca wyniki w formacie null-terminated, co jest przydatne w skryptach, które przetwarzają wiele ścieżek.
- `--help`: Wyświetla pomoc dotyczącą użycia polecenia.
- `--version`: Wyświetla wersję polecenia.

## Common Examples
1. Wyodrębnienie katalogu z pełnej ścieżki:
   ```bash
   dirname /home/użytkownik/dokumenty/plik.txt
   ```
   Wynik: `/home/użytkownik/dokumenty`

2. Użycie z wieloma argumentami:
   ```bash
   dirname /usr/local/bin/skrypt.sh /etc/konfiguracja.conf
   ```
   Wynik:
   ```
   /usr/local/bin
   /etc
   ```

3. Użycie z opcją `-z`:
   ```bash
   dirname -z /var/log/system.log
   ```
   Wynik: `/var/log` (w formacie null-terminated)

## Tips
- Używaj `dirname` w skryptach, aby łatwo uzyskać ścieżki katalogów, co może być przydatne przy tworzeniu nowych plików w tym samym katalogu.
- Możesz łączyć `dirname` z innymi poleceniami, takimi jak `basename`, aby uzyskać zarówno katalog, jak i nazwę pliku z pełnej ścieżki.
- Pamiętaj, że `dirname` nie dodaje ukośników na końcu zwracanej ścieżki, co może być istotne przy dalszym przetwarzaniu.