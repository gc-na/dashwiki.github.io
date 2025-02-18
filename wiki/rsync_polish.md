# [Debian] Debian Almquist Shell (dash) rsync użycie: Synchronizacja plików i katalogów

## Overview
Rsync to potężne narzędzie do synchronizacji plików i katalogów między różnymi lokalizacjami. Umożliwia przesyłanie danych zarówno lokalnie, jak i przez sieć, z zachowaniem struktury katalogów oraz atrybutów plików.

## Usage
Podstawowa składnia polecenia rsync jest następująca:

```bash
rsync [options] [arguments]
```

## Common Options
- `-a` – tryb archiwum; synchronizuje pliki i katalogi, zachowując atrybuty.
- `-v` – tryb szczegółowy; wyświetla szczegóły operacji.
- `-z` – kompresja danych podczas transferu.
- `-r` – rekurencyjnie synchronizuje katalogi.
- `--delete` – usuwa pliki w docelowej lokalizacji, które nie istnieją w źródłowej.

## Common Examples
1. Synchronizacja lokalnego katalogu z innym katalogiem:
   ```bash
   rsync -av /ścieżka/do/źródła/ /ścieżka/do/celu/
   ```

2. Synchronizacja plików z lokalnego katalogu do zdalnego serwera:
   ```bash
   rsync -avz /ścieżka/do/źródła/ użytkownik@serwer:/ścieżka/do/celu/
   ```

3. Synchronizacja z usunięciem plików, które nie istnieją w źródle:
   ```bash
   rsync -av --delete /ścieżka/do/źródła/ /ścieżka/do/celu/
   ```

4. Synchronizacja z kompresją:
   ```bash
   rsync -avz /ścieżka/do/źródła/ użytkownik@serwer:/ścieżka/do/celu/
   ```

## Tips
- Zawsze używaj opcji `-n` (dry run), aby zobaczyć, co zostanie zrobione przed faktycznym wykonaniem polecenia.
- Używaj opcji `-e` do określenia zdalnego protokołu, np. SSH, jeśli synchronizujesz przez sieć.
- Regularnie twórz kopie zapasowe ważnych danych, aby uniknąć ich utraty podczas synchronizacji.