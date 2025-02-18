# [Debian] Debian Almquist Shell (dash) df użycie: Sprawdzanie dostępnej przestrzeni dyskowej

## Overview
Polecenie `df` w systemie Linux służy do wyświetlania informacji o dostępnej i używanej przestrzeni na systemach plików. Umożliwia użytkownikom monitorowanie wykorzystania dysku oraz identyfikowanie potencjalnych problemów z przestrzenią.

## Usage
Podstawowa składnia polecenia `df` wygląda następująco:

```bash
df [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `df`:

- `-h`: Wyświetla rozmiary w formacie czytelnym dla ludzi (np. KB, MB, GB).
- `-T`: Wyświetla typ systemu plików dla każdego zamontowanego systemu plików.
- `-a`: Wyświetla wszystkie systemy plików, w tym te, które mają zero dostępnej przestrzeni.
- `-i`: Wyświetla informacje o inode'ach zamiast przestrzeni dyskowej.

## Common Examples

1. **Podstawowe użycie**: Wyświetlenie informacji o wszystkich zamontowanych systemach plików.
   ```bash
   df
   ```

2. **Czytelny format**: Wyświetlenie informacji w formacie przyjaznym dla użytkownika.
   ```bash
   df -h
   ```

3. **Typ systemu plików**: Wyświetlenie informacji z typami systemów plików.
   ```bash
   df -T
   ```

4. **Informacje o inode'ach**: Wyświetlenie informacji o dostępnych inode'ach.
   ```bash
   df -i
   ```

5. **Wyświetlenie wszystkich systemów plików**: W tym również tych, które mają zero dostępnej przestrzeni.
   ```bash
   df -a
   ```

## Tips
- Regularnie monitoruj przestrzeń dyskową, aby uniknąć problemów z brakiem miejsca.
- Używaj opcji `-h`, aby łatwiej interpretować wyniki.
- Jeśli pracujesz z wieloma systemami plików, opcja `-T` może być przydatna do szybkiej identyfikacji typów systemów plików.