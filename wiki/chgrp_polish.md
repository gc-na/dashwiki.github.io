# [Polski] Debian Almquist Shell (dash) chgrp użycie: Zmiana grupy plików

## Overview
Polecenie `chgrp` służy do zmiany grupy przypisanej do plików i katalogów w systemie Unix/Linux. Umożliwia to administratorom i użytkownikom zarządzanie dostępem do zasobów w systemie.

## Usage
Podstawowa składnia polecenia `chgrp` jest następująca:

```
chgrp [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `chgrp`:

- `-R` : Rekursywnie zmienia grupę dla katalogów i ich zawartości.
- `-v` : Wyświetla szczegóły dotyczące zmiany grupy dla każdego pliku.
- `-c` : Wyświetla tylko pliki, dla których zmiana grupy się powiodła.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `chgrp`:

1. Zmiana grupy pliku na "developers":
   ```bash
   chgrp developers plik.txt
   ```

2. Rekursywna zmiana grupy katalogu na "admins":
   ```bash
   chgrp -R admins katalog/
   ```

3. Wyświetlenie szczegółów zmiany grupy dla pliku:
   ```bash
   chgrp -v developers plik.txt
   ```

4. Zmiana grupy dla wielu plików jednocześnie:
   ```bash
   chgrp developers plik1.txt plik2.txt plik3.txt
   ```

## Tips
- Upewnij się, że masz odpowiednie uprawnienia do zmiany grupy plików.
- Używaj opcji `-R` ostrożnie, aby nie zmienić grupy dla niezamierzonych plików.
- Sprawdzaj grupę plików po użyciu polecenia `chgrp` za pomocą polecenia `ls -l`, aby upewnić się, że zmiany zostały zastosowane.