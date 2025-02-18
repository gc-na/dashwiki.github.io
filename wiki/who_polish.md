# [Debian] Debian Almquist Shell (dash) who: wyświetlanie zalogowanych użytkowników

## Overview
Polecenie `who` w systemie Linux służy do wyświetlania listy użytkowników aktualnie zalogowanych do systemu. Informacje te mogą być przydatne do monitorowania aktywności użytkowników oraz do zarządzania systemem.

## Usage
Podstawowa składnia polecenia `who` jest następująca:

```bash
who [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `who`:

- `-b`: Wyświetla czas ostatniego uruchomienia systemu.
- `-q`: Wyświetla tylko listę użytkowników oraz ich liczbę.
- `-H`: Wyświetla nagłówki kolumn w wynikach.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `who`:

1. Wyświetlenie listy wszystkich zalogowanych użytkowników:
   ```bash
   who
   ```

2. Wyświetlenie czasu ostatniego uruchomienia systemu:
   ```bash
   who -b
   ```

3. Wyświetlenie tylko liczby zalogowanych użytkowników:
   ```bash
   who -q
   ```

4. Wyświetlenie listy użytkowników z nagłówkami kolumn:
   ```bash
   who -H
   ```

## Tips
- Używaj opcji `-H`, aby uzyskać bardziej czytelne wyniki, zwłaszcza gdy przeglądasz dużą liczbę użytkowników.
- Możesz łączyć różne opcje, aby dostosować wyniki do swoich potrzeb, na przykład `who -b -H`.
- Regularne sprawdzanie zalogowanych użytkowników może pomóc w identyfikacji nieautoryzowanych dostępów do systemu.