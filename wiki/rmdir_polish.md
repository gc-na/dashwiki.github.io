# [Polski] Debian Almquist Shell (dash) rmdir użycie: Usuwa puste katalogi

## Overview
Polecenie `rmdir` służy do usuwania pustych katalogów w systemie plików. Jeśli katalog zawiera jakiekolwiek pliki lub inne katalogi, `rmdir` nie będzie w stanie go usunąć i zgłosi błąd.

## Usage
Podstawowa składnia polecenia `rmdir` jest następująca:

```
rmdir [opcje] [argumenty]
```

## Common Options
- `--ignore-fail-on-non-empty`: Ignoruje błędy, jeśli katalog nie jest pusty.
- `--parents`: Usuwa katalogi w hierarchii, jeśli są puste, zaczynając od najniższego poziomu.
- `-p`: Skrót dla opcji `--parents`.

## Common Examples
1. Usunięcie pustego katalogu:
   ```bash
   rmdir moj_katalog
   ```

2. Usunięcie kilku pustych katalogów jednocześnie:
   ```bash
   rmdir katalog1 katalog2 katalog3
   ```

3. Usunięcie pustego katalogu z użyciem opcji `--parents`:
   ```bash
   rmdir --parents /sciezka/do/pustego/katalogu
   ```

4. Ignorowanie błędów, gdy katalog nie jest pusty:
   ```bash
   rmdir --ignore-fail-on-non-empty moj_katalog
   ```

## Tips
- Upewnij się, że katalog jest pusty przed użyciem `rmdir`, aby uniknąć błędów.
- Możesz użyć polecenia `ls` przed `rmdir`, aby sprawdzić zawartość katalogu.
- Jeśli chcesz usunąć katalog i jego zawartość, rozważ użycie polecenia `rm -r` zamiast `rmdir`.