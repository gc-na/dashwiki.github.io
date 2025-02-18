# [Debian] Debian Almquist Shell (dash) mkdir użycie: Tworzenie katalogów

## Overview
Polecenie `mkdir` służy do tworzenia nowych katalogów w systemie plików. Umożliwia użytkownikom organizowanie plików w struktury katalogów, co ułatwia zarządzanie danymi.

## Usage
Podstawowa składnia polecenia `mkdir` jest następująca:

```
mkdir [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `mkdir`:

- `-p` – Tworzy katalogi nadrzędne, jeśli nie istnieją.
- `-m` – Ustala uprawnienia dla nowego katalogu (w formacie oktalnym).
- `--help` – Wyświetla pomoc dotyczącą polecenia.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `mkdir`:

1. Tworzenie pojedynczego katalogu:
   ```bash
   mkdir nowy_katalog
   ```

2. Tworzenie wielu katalogów jednocześnie:
   ```bash
   mkdir katalog1 katalog2 katalog3
   ```

3. Tworzenie katalogu z nadrzędnym katalogiem, jeśli nie istnieje:
   ```bash
   mkdir -p /ścieżka/do/katalogu/nadrzędnego/nowy_katalog
   ```

4. Ustalanie uprawnień dla nowego katalogu:
   ```bash
   mkdir -m 755 nowy_katalog
   ```

## Tips
- Zawsze używaj opcji `-p`, gdy tworzysz złożoną strukturę katalogów, aby uniknąć błędów, gdy katalog nadrzędny nie istnieje.
- Sprawdzaj uprawnienia katalogu po jego utworzeniu, aby upewnić się, że są odpowiednie dla Twoich potrzeb.
- Używaj opisowych nazw katalogów, aby łatwiej było je później zidentyfikować.